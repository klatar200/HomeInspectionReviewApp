# DECISIONS (append-only; supersede ✗edit; AS-OF dates; status: DECIDED|PROPOSED|OPEN)

D-001 2026-10-13 DECIDED region=Plainfield IL (Will Co.) + configurable radius. Default radius PROPOSED 25mi [radius SUPERSEDED-BY D-015]. Supersedes agent's Phoenix recommendation. Why: Keagan is local; Phoenix/CyFy = illustrative example only. Downside: IL builder/inspector landscape unaudited (RESEARCH.md §3).
D-002 2026-10-13 DECIDED first user=new-build buyers.
D-003 2026-10-13 DECIDED review model v1=structured fields + free text; revisit after research. Fields in PLAN.md §Data.
D-004 2026-10-13 DECIDED verification v1=honor system. PROPOSED mitigations (need Keagan OK): email-verified account to post; rate limit; "unverified" badge on reviews w/o uploaded report; builder-conflict flags REQUIRE evidence upload (see D-008). Failure mode: builder/competitor astroturf + defamation-bait; mitigations reduce, ✗eliminate.
D-005 2026-10-13 DECIDED second-opinion feature=yes. Condition (agent-recommended, accepted by "Yes"): private data only until legal review. ✗public naming of "missed defects" pre-review.
D-006 2026-10-13 DECIDED availability=link-out to inspector booking URL. ✗calendar sync v1.
D-007 2026-10-13 DECIDED free inspector profiles; ✗pay-to-rank; ✗paid placement EVER (permanent; would recreate builder-steering conflict).
D-008 2026-10-13 DECIDED builder-conflict tracking=yes, documented evidence only. Accepted: highest legal-attack surface.
D-009 2026-10-13 DECIDED legal=no counsel available. Written policy "verified facts only" REQUIRED before public launch (launch blocker, PLAN G2). Not legal advice; re-assess if any demand letter arrives.
D-010 2026-10-13 DECIDED stack=React/TS · Node/Fastify · Prisma/Postgres; $0 during build+test. Hosting choice DEFERRED to deploy phase (RESEARCH.md §4).
D-011 2026-10-13 DECIDED goal=revenue-driven passion project; build solid first, monetization deferred; money ≠ immediate goal. Monetization options must satisfy D-007.
D-012 2026-10-13 DECIDED(by omission) Keagan declined to set a kill/decision date ("not sure how deep; won't abandon"). Agent holds PROPOSED milestone gates instead (PLAN.md §Gates); NOT agreed. Agent restates gates at each check-in per global rules.
D-013 2026-10-13 DECIDED git workflow=commit directly to main (explicit permission to push main; remote had no main). Branch claude/trusting-dijkstra-ex56mr kept only as session branch.
D-014 2026-10-13 DECIDED seed unclaimed inspector profiles from public IDFPR data; Keagan asked for a deep-research plan → RESEARCH.md §5 + PLAN.md "Seed plan". Source verified: official IDFPR open-data registry (ODbL).
D-015 2026-10-13 DECIDED default search radius=50mi from Plainfield 60544 (supersedes D-001's 25mi). Effect: ≈ all of Chicagoland (1169 active individual licensees at AS-OF 2026-10-13, RESEARCH §5). "Local" framing is wide; per-profile distance still shown.
D-016 2026-10-13 DECIDED no known local new-build contacts. Validation interviews + marketing channel = OPEN (Keagan: marketing undecided).
D-017 2026-10-13 DECIDED working title="Inspec". Public branding NOT final; ✗domain/trademark checks done.
D-018 2026-10-13 DECIDED accounts required to post reviews (email magic-link).
D-019 2026-10-13 DECIDED first marketing channel=social media (platform/accounts/content OPEN). Closes Q-1 channel only; first-reviewer sourcing still OPEN. Spend=$0 until opt-in.
D-020 2026-10-13 DECIDED company link=inspector self-declares company on their claimed profile (labelled "self-reported"); no admin entity↔individual matching. Supersedes PLAN Q-3. Downside: false company claims ⇒ claim review checks license ownership only; company text is ✗verified.
D-021 2026-10-13 DECIDED legal review approved in principle: ≈1 hour consult, Keagan to choose counsel + confirm cost (spend ⇒ his decision). Packet=CONTENT_POLICY.md (exists, draft v0.1) (draft + questions for counsel). Launch still blocked until policy finalized (G2).
D-022 2026-10-13 DECIDED "Inspec" = working brand name (reaffirms D-017; no domain/trademark check yet).
D-023 2026-10-13 DECIDED reviews may target EITHER an inspector OR a builder. Reviewed party may challenge; each challenge decided case-by-case by a human moderator. D-008 stands for BuilderFlags (evidence-required structured records); builder REVIEWS are experience-based and need no file. Risk accepted knowingly: builder reviews on honor system = highest defamation/litigation surface; solo-moderator queue does not scale; a builder with counsel can flood challenges. Mitigations PROPOSED in CONTENT_POLICY.md §5.
D-024 2026-10-13 DECIDED challenge process in CONTENT_POLICY.md §5 adopted as working v0.1 (7d reviewer response, 14d decision, keep-visible-unless-facially-violating, 1 appeal); Keagan will alter after counsel feedback. Closes PLAN Q-3.
D-025 2026-10-13 DECIDED builder claim verification v1=company-email domain. Downside: free-mail/shared domains ⇒ manual check fallback. Closes PLAN Q-4.
D-026 2026-10-13 DECIDED first social channel=Facebook (groups/pages/community posts). Refines D-019. Account owner + content plan OPEN. ToS/spam rules of target groups ✗checked ⇒ read each group's rules before posting.
