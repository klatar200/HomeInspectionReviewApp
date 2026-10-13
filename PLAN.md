# PLAN — Inspec (working title, D-017) (FUTURE only; checkboxes; shipped work → SHIPPED.md when exists). Decisions: DECISIONS.md. Research: RESEARCH.md.

## Product
Review + discovery site for residential home inspectors within 50mi of Plainfield IL (D-015), first audience=new-build buyers. Reviews can target an inspector OR a builder (D-023); reviewed party can challenge, decided case-by-case. Headline trust signal = transparent evidence counts, stars secondary (D-028). Differentiators: structured/evidence-backed reviews; builder-conflict flags (evidence-only, D-008); private second-opinion comparison. ✗pay-to-rank EVER (D-007).

## Design notes
Journeys (D-034): A builder researcher (pre-commit; searches builder/neighborhood) · B budget buyer (wants inspector who holds builder accountable; filters by new-construction services: pre-drywall / final / 11-month warranty / resale, self-declared at claim). Builder-page trust signals analogous to D-028 (counts, not a black-box score) = TBD.
Primary entry = post-burn users (D-030). Builder due-diligence beyond reviews (deposit loss, litigation) NOT in scope pending D-031.

## Scope v1 (IN)
inspector directory+profiles · radius search · accounts (email magic-link) · reviews of inspectors AND builders (structured+text) · report/evidence upload · builder pages + communities (user-created, admin-merged) + builder claim · evidence-backed flags · inspector claim flow (self-declared company, D-020) · challenge/dispute flow · booking link-out · moderation queue · takedown/dispute form · written content policy.
## OUT v1 (deferred, reasons)
calendar sync (D-006) · payments/lead-gen (D-011) · mobile app · public second-opinion (D-005 legal) · multi-region · inspector-paid anything (D-007).

## Data (Prisma/Postgres; every row scoped; ✗client-supplied identity — userId from session only)
- User(id,email,role[buyer|inspector|admin],createdAt)
- Inspector(id,kind[individual|entity],displayName,idfprLicenseNo UNIQUE,licenseStatus,origIssueDate,expirationDate,city,state,zip(server-only),lat,lng,everDisciplined,source='idfpr',sourceSyncedAt,bookingUrl?,claimedByUserId?,status[unclaimed|claimed|removed])
- LicenseDiscipline(id,inspectorId,caseNumber,action,reason,startDate,endDate)  — verbatim from IDFPR, many per Inspector
- Community(id,name,city,state,createdByUserId,status[active|merged|removed],mergedIntoId?)  — a residential neighborhood/subdivision; user-created, admin-merged (D-034 PROPOSED); many-to-many with Builder
- Builder(id,name,aliases[],region,claimedByUserId?,createdByUserId,status[active|merged|removed],mergedIntoId?)  — created by reviewers; admin merges dupes; claim=company-email verification
- Dispute(id,reviewId,raisedByUserId,raisedByRole[inspector|builder],reason[factually_false|no_relationship|policy_violation|other],statement,evidenceIds[],status[open|upheld_kept|removed|annotated],decisionNote,decidedByAdminId?,openedAt,decidedAt?)  — reviewer notified, can respond; decision logged in ModerationAction
- Review(id,authorId,targetType[inspector|builder],inspectorId?,builderId?,communityId?,builderStage?[pre_construction|under_construction|closed],builderStatus?[delivered|delayed|not_started|contract_cancelled],reviewerRelationship[hired_inspector|bought_from_builder|other],inspectionType[pre_close|10day_post|11mo_warranty|resale|other],inspectedOn,hoursOnSite?,defectsReported?,accessRestricted?bool,reportUploaded bool,rating 1-5,body,tier[unverified|report_attached],status[pending|published|removed],createdAt)  — fields neutral; NO leading prompts (RESEARCH §4 Sec.230)
- Evidence(id,ownerId,reviewId?|flagId?,fileKey,mime,sha256,createdAt)  — private bucket, signed URLs
- BuilderFlag(id,builderId,type[access_restricted|steered_inspector|disparaged_inspector],evidenceIds[≥1 REQUIRED],authorId,status,createdAt)
- SecondOpinion(id,ownerId,priorReportKey,laterReportKey,notes) — PRIVATE to owner only (D-005)
- ZipCentroid(zip,lat,lng) — Census ZCTA public data; radius=haversine (default 50mi); ✗external geocode API ($0)
- ModerationAction(id,adminId,targetType,targetId,action,reason,createdAt) · TakedownRequest(id,requesterEmail,targetId,claim,evidenceUrl?,status)
Security: cross-user access → 404 ✗403; allowlist validation on all inputs (zod); upload mime/size allowlist; rate limits; no secrets in repo.

## Wireframes (ASCII; low-fi; mobile-first)
W1 Home/Search
```
[LOGO]                         [Sign in]
Tabs: [Research a builder / neighborhood]   [Find an inspector]
(Inspector tab) [ ZIP 60544 ] [ 50 mi v ] [ New-build services v ] [Search]
(Builder tab)   [ Builder or neighborhood name ] [ ZIP ] [ 50 mi v ] [Search] → rows: builder · n reviews · stages · communities nearby
-- Results (sorted: reviews+evidence, ✗paid) ---------------
| Name · Co.   12 reviews · 8 with report · avg 4.5h on site · ★4.8   License: Active(checked 10/13) |
| 9.2 mi · New-build ✓ · [View] [Book ↗]                                        |
```
W2 Inspector profile
```
Name · Co.  License #### Active (checked date)   [Book ↗ (external)]
12 reviews | 8 with report | Avg hours on site 4.5 | Avg items found n | ★4.8 (secondary)
Builders they've inspected: [Builder A (5)] [Builder B (2)]
Tabs: Reviews | About | Service area
Review card: ★ · type · date · [report attached]/[unverified] · body · [Report problem]
[Write a review]   [Claim this profile] (if unclaimed)
```
W3 Write review (stepper)
```
0 Review an [Inspector] or a [Builder]?
1 Pick target (+ builder/inspector involved, optional)  2 Inspection type/date/hours  3 What was found (count + free text)
4 Access: "Was the inspector able to access ___?" (neutral yes/no/NA)  5 Upload report (optional → badge)  6 Preview+Submit (policy checkbox)
```
W4 Builder page
```
Builder A  [Claim this builder]   Reviews (n) | Evidence-backed flags (n)
Review card: ★ · relationship (bought a home / other) · date · body · builder reply · [Disputed: under review]? · [Challenge this review]
Flag: "Restricted inspector access" · evidence: [PDF][photo] · date · [Dispute this]
Disclaimer: flags show submitted evidence, ✗app verdict.
```
W5 Second-opinion (private; owner only)
```
Upload prior report | Upload later report | Notes → side-by-side. Visible to you only. [Delete]
```
W6 Inspector/builder dashboard: claimed profile edit (booking URL, bio, company [self-reported]), public reply to reviews, [Challenge] a review (reason + statement + evidence).
W8 Challenge flow: reviewed party picks reason → statement/evidence → submit → reviewer notified + can respond → moderator decision shown on review (kept / removed / annotated) with reason code.
W7 Admin moderation queue: pending reviews/flags, open challenges (oldest first, clock shown), evidence viewer, remove/restore/annotate w/ reason, takedown inbox.

## Phases (each ends w/ binary check)
- [x→DRAFT] P0b CONTENT_POLICY.md draft exists (counsel packet). TODO: Keagan picks lawyer+confirms cost (D-021); incorporate counsel feedback; finalize. LAUNCH BLOCKER (G2).
- [ ] P1 Schema+API: Prisma models, ZipCentroid import, radius search endpoint, auth (magic-link), authz tests (cross-user probe→404).
- [ ] P2 Web: W1,W2,W3 end-to-end locally. Check: seeded inspector → review submit → appears after moderation.
- [ ] P3 Moderation (W7) + challenge flow (W8, Dispute model) + takedown form + audit log. Check: challenge → reviewer notified → decision recorded w/ reason code → visible on review.
- [ ] P4 Builders (W4): user-created builder pages + admin merge + builder claim + reviews of builders + evidence-required flags.
- [ ] P5 Inspector claim/dashboard (W6) + booking link-out.
- [ ] P6 Second-opinion private (W5).
- [ ] P7 Seed from IDFPR open data (see Seed plan) + local audit of builders (RESEARCH §3 gap).
- [ ] P8 Deploy ($0 stack verified ToS-for-commercial-use first; D-010) + pilot.

## Gates (PROPOSED, NOT AGREED — D-012; agent restates every check-in)
G1 P2 end-to-end locally working. G2 CONTENT_POLICY written + takedown flow live (blocks public launch). G3 pilot: ≥10 CLAIMED inspector profiles AND ≥25 reviews within 90d of launch (seeding alone ≈1169 profiles, ✗counts), else stop-or-pivot decision. Sunk cost ≠ evidence.

## Seed plan (D-014; facts+risks: RESEARCH §5)
Goal: ≈1169 active individual + 116 entity IDFPR licensees within 50mi preloaded as UNCLAIMED, license-facts-only profiles. $0.
Steps (each has a binary check):
- [ ] S1 Fetch: SoQL on pzzh-kp68 with FILTER from RESEARCH §5, page via $limit/$offset ordered by license_number. Check: statewide ACTIVE counts match live API (query count()), not a stale constant.
- [ ] S2 Zip→lat/lng: import Census 2023 ZCTA gazetteer into ZipCentroid; unmatched zips logged, profile kept with null geo + excluded from radius search. Check: 60544 → 41.6139,-88.2187.
- [ ] S3 Normalize+dedupe: aggregate rows by license_number → Inspector; discipline rows → LicenseDiscipline; title-case names; keep raw row hash. Check: distinct licenses == distinct Inspector rows (1806 at 2026-10-13 snapshot incl. non-radius).
- [ ] S4 Idempotent upsert on idfprLicenseNo; sync weekly (cron/GitHub Action, $0); status change → update; vanished record → mark stale, ✗delete. Check: run twice ⇒ identical row counts; test w/ fixture of status change.
- [ ] S5 Radius filter (haversine) as query. Check: ≤50mi from 60544 ⇒ ≈1169 individuals/116 entities (±drift; record AS-OF date); ≤25mi ⇒ ≈423/41.
- [ ] S6 Display rules: name, license no, status, issue/expiry, CITY only (✗zip, ✗street), discipline facts verbatim + dates, "Source: IDFPR via Illinois Open Data Portal (ODbL) · synced <date> · verify at IDFPR lookup" on every profile. ✗bulk export/API of seeded data. ✗ratings derived from discipline.
- [ ] S7 Claim flow: claimant proves license ownership (matches name+license no. + email verification by admin review v1) → can add bookingUrl/bio/serviceArea. Removal-request form for non-license content.
- [ ] S8 Contact enrichment: NONE automated v1 ($0, ToS). Manual/claim only. Revisit w/ dated evidence on ILASHI/InterNACHI directory terms.
- [ ] S9 Tests: dedupe, idempotency, radius math vs known pair, discipline rendered verbatim, cross-user claim probe→404, zip never in API response.

## Open questions
(none blocking. Deferred to near launch, D-027: Facebook account/owner, counsel choice+cost, first-reviewer sourcing.)
