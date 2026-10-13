# Inspec — Content Policy (DRAFT v0.1, 2026-10-13) + Questions for Counsel

STATUS: DRAFT for attorney review (D-021). Not final, not legal advice, not yet public. Public wording needs Keagan's approval. Launch is blocked until this is finalized (PLAN G2).

## 1. What Inspec is
A review and discovery site for residential home inspectors and home builders near Plainfield, Illinois (50-mile radius). Reviews are opinions based on the reviewer's own experience. Inspec does not inspect homes, does not certify anyone, and does not give legal or professional advice.

## 2. Who can write a review
- Signed-in users only (email link). One review per person per inspector or builder per transaction.
- Reviewer states their relationship (hired this inspector / bought a home from this builder / other). This is self-reported (honor system v1); reviews that attach a report or contract page are labelled "report attached".

## 3. What a review may contain
- First-hand experience: what happened, when, what you were told, what you saw.
- Facts you can support. Opinions clearly stated as opinions.
- Neutral structured fields (inspection type, date, hours on site, number of items found, whether the inspector could access the areas they needed).
Not allowed (removed on report or review): threats or harassment; private personal information (phone numbers, home addresses, family details); accusations of crimes presented as fact without evidence; reviews of a business you have no first-hand relationship with; content posted by the business itself or its competitors about each other; reviews written in exchange for payment, discounts, or favors; copied content you do not have the right to post; anything the law requires us to remove.
Inspec does not suggest or require accusations. Review prompts are neutral by design.

## 4. Evidence and uploads
- Uploads (photos, report pages, contract pages) must be the uploader's to share. Reports may contain the inspector's work product; the reviewer is responsible for having the right to share it.
- Builder FLAGS (structured records such as "restricted inspector access") require at least one evidence file and show the evidence, not an Inspec verdict.

## 5. Challenges (PROPOSED — confirm or edit)
Who: the reviewed inspector or builder, after verifying their profile. Anyone else uses the report button.
How: pick a reason (factually false / no relationship / policy violation / other), add a statement and optional evidence.
Process:
1. Reviewer is told a challenge was filed and may respond (7 days).
2. The review stays visible while under review unless it appears to violate §3 on its face (e.g., private information, threats). A neutral "challenged" note is shown. [Counsel Q3]
3. A human moderator decides case by case, within 14 days of the response window, using only the review, statement, evidence, and response. Outcomes: KEPT, REMOVED (reason code), or ANNOTATED (party's response shown).
4. A negative review is not removed because it is negative. A business cannot pay for removal or ranking, ever.
5. The decision and reason code are recorded; both sides are told. One appeal, reviewed by a different person if available (currently the same moderator — disclosed limitation).
Legal demands (court order, attorney letter) go to a separate takedown inbox and are handled per counsel's guidance.

## 6. License data on inspector profiles
Shown from the State of Illinois open data portal (IDFPR professional license registry, ODbL license): name, license number, status, dates, city, and disciplinary records exactly as published, with the "as of" date and a link to verify at IDFPR. Inspec does not summarize, score, or rank by disciplinary history. Inspectors may claim a profile to add a booking link, bio, and company name (self-reported, not verified). Removal requests for non-license content are honored per this policy.

## 7. Money
No paid placement and no pay-to-rank, ever. Profiles are free. [PLAN D-007]

---
## Questions for counsel (ranked; ~1 hour: do 1–5 first)
1. Section 230 posture. Given neutral structured review fields, human case-by-case challenge decisions, "challenged"/"annotated" labels, and platform-authored content (license facts from IDFPR, "report attached" badges): does any of this risk losing immunity for user reviews? What wording to avoid?
2. Builder reviews. What is the exposure to defamation, trade libel, or tortious interference claims from builders (including via builder purchase-contract non-disparagement clauses and the federal Consumer Review Fairness Act)? Any Illinois anti-SLAPP (Citizen Participation Act) considerations for reviewers and for us? [my recollection of that act is UNVERIFIED]
3. Challenge handling. Keep-visible-during-review vs remove-on-challenge: which is safer for us? Is a "challenged" label advisable?
4. Business structure. Should an LLC (or similar) hold this before launch? Insurance (media liability) worth it at $0 revenue?
5. Terms of Service + Privacy Policy. Minimum viable set: user indemnity, content license, arbitration or not, dispute/takedown clause, DMCA agent for uploaded evidence, governing law.
6. Uploaded inspection reports: copyright and confidentiality (inspection agreements may restrict sharing). What do we require of uploaders?
7. Displaying IDFPR disciplinary records: any Illinois-specific limits, accuracy/staleness duties, or required disclaimers? ODbL attribution wording; is "no bulk export/API" the right reading of share-alike?
8. FTC rule on fake/incentivized reviews: what must the honor-system v1 do to stay compliant (e.g., inspectors soliciting reviews)?
9. Second-opinion feature (private, user-only, compares two reports): liability for storing third-party reports; retention and deletion rules.
10. Responding to subpoenas or demands to reveal a reviewer's identity: what policy and data retention?
11. Moderator conflicts: sole founder as only decision-maker — disclosures or process changes advisable?
12. Any Illinois or federal licensing or advertising rules for a site that rates licensed professionals?
13. Structured builder-review status fields (home delivered / delayed / construction not started / contract cancelled; stage): are these neutral enough under the Section 230 participation concern, and are there wording changes you'd advise?
14. Inspector-provided sample reports: copyright/ownership, client-PII redaction duty, and how to label so it is not mistaken for a real client report.
15. Structured outcome/status fields and app-computed counts about named builders and inspectors (e.g., "inspection-reported items addressed: none", "inspector access: restricted"): does designing these fields and showing counts make Inspec a content developer under Section 230 (cf. Roommates.com)? Is a minimum-reviews threshold and a "reported by reviewers" label enough? Also: any terms issues linking to or displaying Google/Yelp ratings?
