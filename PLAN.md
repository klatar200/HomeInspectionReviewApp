# PLAN (FUTURE only; checkboxes; shipped work → SHIPPED.md when exists). Decisions: DECISIONS.md. Research: RESEARCH.md.

## Product
Review + discovery site for residential home inspectors near Plainfield IL (radius search), first audience=new-build buyers. Differentiators: structured/evidence-backed reviews; builder-conflict records (evidence-only); private second-opinion comparison. ✗pay-to-rank EVER (D-007).

## Scope v1 (IN)
inspector directory+profiles · radius search · accounts (email magic-link) · reviews (structured+text) · report/evidence upload · builder pages + evidence-backed flags · inspector claim flow · booking link-out · moderation queue · takedown/dispute form · written content policy.
## OUT v1 (deferred, reasons)
calendar sync (D-006) · payments/lead-gen (D-011) · mobile app · public second-opinion (D-005 legal) · multi-region · inspector-paid anything (D-007).

## Data (Prisma/Postgres; every row scoped; ✗client-supplied identity — userId from session only)
- User(id,email,role[buyer|inspector|admin],createdAt)
- Inspector(id,name,company,idfprLicenseNo?,licenseStatus?,licenseCheckedAt?,serviceZips[],bookingUrl,claimedByUserId?,status[unclaimed|claimed])
- Builder(id,name,aliases[],region)
- Review(id,authorId,inspectorId,builderId?,inspectionType[pre_close|10day_post|11mo_warranty|resale|other],inspectedOn,hoursOnSite?,defectsReported?,accessRestricted?bool,reportUploaded bool,rating 1-5,body,tier[unverified|report_attached],status[pending|published|removed],createdAt)  — fields neutral; NO leading prompts (RESEARCH §4 Sec.230)
- Evidence(id,ownerId,reviewId?|flagId?,fileKey,mime,sha256,createdAt)  — private bucket, signed URLs
- BuilderFlag(id,builderId,type[access_restricted|steered_inspector|disparaged_inspector],evidenceIds[≥1 REQUIRED],authorId,status,createdAt)
- SecondOpinion(id,ownerId,priorReportKey,laterReportKey,notes) — PRIVATE to owner only (D-005)
- ZipCentroid(zip,lat,lng) — Census ZCTA public data; radius=haversine; ✗external geocode API ($0)
- ModerationAction(id,adminId,targetType,targetId,action,reason,createdAt) · TakedownRequest(id,requesterEmail,targetId,claim,evidenceUrl?,status)
Security: cross-user access → 404 ✗403; allowlist validation on all inputs (zod); upload mime/size allowlist; rate limits; no secrets in repo.

## Wireframes (ASCII; low-fi; mobile-first)
W1 Home/Search
```
[LOGO]                         [Sign in]
Find a home inspector near you
[ ZIP 60544 ] [ 25 mi v ] [ New-build experience v ] [Search]
-- Results (sorted: reviews+evidence, ✗paid) ---------------
| Name · Co.   ★4.8 (12)  [report-attached 8]   License: Active(checked 10/13) |
| 9.2 mi · New-build ✓ · [View] [Book ↗]                                        |
```
W2 Inspector profile
```
Name · Co.  License #### Active (checked date)   [Book ↗ (external)]
★4.8 | 12 reviews | 8 with report | Avg hours on site 4.5
Builders they've inspected: [Builder A (5)] [Builder B (2)]
Tabs: Reviews | About | Service area
Review card: ★ · type · date · [report attached]/[unverified] · body · [Report problem]
[Write a review]   [Claim this profile] (if unclaimed)
```
W3 Write review (stepper)
```
1 Inspector+Builder(optional)  2 Inspection type/date/hours  3 What was found (count + free text)
4 Access: "Was the inspector able to access ___?" (neutral yes/no/NA)  5 Upload report (optional → badge)  6 Preview+Submit (policy checkbox)
```
W4 Builder page
```
Builder A   Reviews mentioning (n) | Evidence-backed flags (n)
Flag: "Restricted inspector access" · evidence: [PDF][photo] · date · [Dispute this]
Disclaimer: flags show submitted evidence, ✗app verdict.
```
W5 Second-opinion (private; owner only)
```
Upload prior report | Upload later report | Notes → side-by-side. Visible to you only. [Delete]
```
W6 Inspector dashboard: claimed profile edit (booking URL, zips, bio), respond to reviews (public reply), dispute report.
W7 Admin moderation queue: pending reviews/flags, evidence viewer, remove/restore w/ reason, takedown inbox.

## Phases (each ends w/ binary check)
- [ ] P0 Foundations: monorepo (web/api), CI (lint+typecheck+test), docker-compose Postgres local ($0). Check: CI green, `npm test` passes.
- [ ] P0b Draft CONTENT_POLICY ("verified facts only", takedown/dispute procedure, evidence rules, neutral-prompt rule). LAUNCH BLOCKER (G2).
- [ ] P1 Schema+API: Prisma models, ZipCentroid import, radius search endpoint, auth (magic-link), authz tests (cross-user probe→404).
- [ ] P2 Web: W1,W2,W3 end-to-end locally. Check: seeded inspector → review submit → appears after moderation.
- [ ] P3 Moderation (W7) + takedown form + audit log.
- [ ] P4 Builders (W4) + evidence-required flags.
- [ ] P5 Inspector claim/dashboard (W6) + booking link-out.
- [ ] P6 Second-opinion private (W5).
- [ ] P7 Seed Plainfield-radius inspectors from public license data (needs source; OPEN Q-A) + local audit of builders/inspectors (RESEARCH §3 gap).
- [ ] P8 Deploy ($0 stack verified ToS-for-commercial-use first; D-010) + pilot.

## Gates (PROPOSED, NOT AGREED — D-012; agent restates every check-in)
G1 P2 end-to-end locally working. G2 CONTENT_POLICY written + takedown flow live (blocks public launch). G3 pilot: ≥10 claimed/seeded inspector profiles in radius AND ≥25 reviews within 90d of launch, else stop-or-pivot decision. Sunk cost ≠ evidence.

## Open questions (answer when ready)
Q-A Seed unclaimed inspector profiles from public IDFPR license data? (rec: yes, license facts only, claim flow to edit; risk: listing people w/o consent — mitigated by factual-only + opt-out). IDFPR data access UNVERIFIED.
Q-B App name/branding (public copy = your call).
Q-C Default radius 25mi OK?
Q-D Do you or people you know live in a Plainfield-area new build (first reviewers + validation interviews)? Marketing channel TBD (Facebook community groups for new subdivisions = candidate, UNVERIFIED).
Q-E Accounts required to post reviews (rec: yes, email magic-link) — confirm.
