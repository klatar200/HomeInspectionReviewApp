# Theme 4: Illinois / Chicago-suburb new-build complaints and legal frame

AS-OF: 2026-10-14. Read-only web research. Nothing here is legal advice (D-009: no counsel available).
Attribution rule: anything about a named builder is "alleged" unless a court or regulator found it.

## 0. Access limits and source warnings (read first)

- **ilga.gov returned HTTP 503 on every WebFetch** (statutes, bills, JCAR rules, all mirrors tried: ilga.gov, www.ilga.gov, lig.ilga.gov, witnessslips.ilga.gov, my.ilga.gov). law.justia.com, regulations.justia.com, casemine.com, legiscan.com, courthousenews.com, builderonline.com, wttw.com returned 403. reddit.com is blocked for both WebSearch and WebFetch, so **no Reddit evidence was gathered** (r/chicagosuburbs, r/chicago, r/firsttimehomebuyer, r/homeowners, r/RealEstate all unreachable). Bash curl was denied by the permission classifier; not worked around.
- **Statute text actually read** (fetched): 68 Ill. Adm. Code 1410.300 (Cornell LII), 225 ILCS 441/15-10 *as excerpted by FindLaw, current as of Jan 1, 2025* (each ground's opening words only), 765 ILCS 77/15(9) (Onecle copy, older version). Everything else from ilga.gov is **seen only in search-result summaries**, flagged "SEARCH-ONLY" below. Re-verify before relying.
- WebFetch summaries were produced by a small model; quotes marked (fetch) were returned by it as verbatim. Court PDFs I read directly with pdftotext are marked (PDF).
- Law-firm blogs conflict with case law in places (e.g. lawkeller.com says warranties "can't be waived ... unless explicitly stated"; Illinois Supreme Court says they can be waived under conditions). Court text controls.
- The Daily Herald "builder won't honor warranty" items are consumer Q&A columns (appear syndicated, not Illinois-specific). Treated as non-evidence of Illinois practice.

---

## 1. Illinois law and enforcement

### 1.1 Home-inspector license act (225 ILCS 441) and rules: conflicts and referral fees

| Field | Detail |
|---|---|
| Issue | Inspector may not take referral compensation from other parties; must disclose interest in property / other services; may not accept contingent assignments |
| Builder | n/a |
| Place | Illinois (statewide) |
| Source date | Rule text per LII (undated, current-ish); statute FindLaw "current as of January 01, 2025" |
| Source type | statute / regulation |
| Strength | STRONG (rule text read); statute STRONG-but-excerpted |

**68 Ill. Adm. Code 1410.300 (Unprofessional Conduct)**, https://www.law.cornell.edu/regulations/illinois/Ill-Admin-Code-tit-68-SS-1410.300 (fetched). Verbatim items:
- (d) "The licensee accepts compensation from another party to the real estate transaction, other than the client, for the same service without the written consent of all parties to the transaction."
- (e) "The licensee offers or accepts compensation, directly or indirectly, from other parties dealing with a client while providing a home inspection as consideration or inducement for the referral of business."
- (f) "The licensee performs additional services but fails to provide written notice of the services and/or to secure written consent by the client of a potential or existing conflict that may exist with the home inspection."
- (g) "The licensee fails to promptly disclose in writing to a client any direct or indirect interest in the subject property and fails to secure written consent of the client."
- (h) "The licensee allows an interest in any business to affect the quality of the results of a home inspection."
- (c) bars disclosing results without client approval except emergencies; (m) bars advising whether the client should proceed with the transaction or giving an opinion of value.

**225 ILCS 441/15-10(a) grounds for discipline**, https://codes.findlaw.com/il/chapter-225-professionsoccupations-and-business-operations/il-st-sect-225-441-15-10/ (fetched; FindLaw truncates each item, so only openings are verbatim):
- (11) "Accepting an inspection assignment when the employment itself is contingent upon ..." (predetermined opinion or contingent fee).
- (20) "Performing a home inspection when the home inspector is providing or may also provide other services ..." (conflict disclosure and consent).
- (29) "Disclosing, except as otherwise required by law, inspection results or client information obtained without ..." (written consent).
- (30) "Providing fees, gifts, waivers of liability, or other forms of compensation or gratuities to persons licensed ..." (real-estate licensees; referral-inducement ban). **Full item text NOT verified** (ilga 503). Item numbers per FindLaw and a search summary; earlier versions numbered differently.
- Repeal date conflicting across search results (Jan 1, 2027 vs 2032). Treat as unverified; check ilga.gov.
- SEARCH-ONLY: discipline up to $25,000 per violation; unlicensed practice civil penalty up to $25,000 per violation.

Implication for Inspec: Illinois rules directly prohibit inspector referral compensation (esp. to real-estate licensees) and require written conflict disclosure. The statute names real-estate licensees; **builder-paid or builder-affiliated inspectors are not named specifically** (rule (d) "another party to the real estate transaction" and (h)/(f) would be the nearest hooks; interpretation is counsel's call).

### 1.2 Buyer/inspector access to a new home before closing

- **Result: none found.** No Illinois statute, rule or case located giving a new-build buyer (or their inspector) a right of access before closing. Searched: statute/rule/bill search for pre-closing inspection of new construction; HB 5454 (below) summary mentions warranty terms only.
- **Caveat:** absence could not be confirmed from ilga.gov statute text (503 on all fetches). "None found" rests on web search only.
- SEARCH-ONLY: SB1727 (94th GA, 2005-06), Residential Inspection Ordinance Act, would have *excluded* "under construction ... not yet occupied" property; no evidence it passed. https://www.ilga.gov/ftp/legislation/94/SB/09400SB1727.htm
- Access is therefore contractual (builder's purchase agreement). MEDIUM/WEAK (absence-of-evidence).

### 1.3 Implied warranty of habitability (IWH) and waiver (case law)

| Case | Date | Holding | Source URL | Strength |
|---|---|---|---|---|
| Petersen v. Hubschman Constr. Co., 76 Ill.2d 31 | May 18, 1979 (Ill. S.Ct.) | Recognized IWH for first purchasers of new houses from builder-vendors; knowing disclaimer allowed | https://static.case.law/ill-2d/76/cases/0031-01.json (fetch) | STRONG (court) |
| Bd. of Managers of Village Centre Condo. Ass'n v. Wilmette Partners, 198 Ill.2d 132 | Nov 21, 2001 | A disclaimer must name the warranty of habitability; "merchantability and fitness" language insufficient | https://static.case.law/ill-2d/198/cases/0132-01.json (fetch) | STRONG |
| Fattah v. Bim, 2016 IL 119365 | May 19, 2016 | First buyer's bargained-for waiver (in exchange for 1-yr express warranty) bars the second purchaser's IWH claim, "as is" resale | PDF read via illinoiscourts.gov (https://www.illinoiscourts.gov/Resources/b0713898-bd1f-419e-93a0-ce05c3276092/119365.pdf) | STRONG |
| Sienna Court Condo. Ass'n v. Champion Aluminum, 2018 IL 122022 | Dec 28, 2018 | No IWH claim against subcontractors lacking contract with purchaser; overruled Minton | https://www.illinoiscourts.gov/files/122022.pdf/opinion (PDF read) | STRONG |

Verbatim (<=25 words):
- Petersen (fetch): "we do not consider a knowing disclaimer of the implied warranty to be against the public policy of this State."
- Petersen (fetch): "any such a disclaimer must be strictly construed against the builder-vendor."
- Fattah ¶21 (PDF): waiver must be "a conspicuous provision that fully discloses its consequences and establishes that the waiver was in fact the agreement reached by the parties."
- Village Centre (fetch): "any disclaimer that does not reference the implied warranty of habitability by name is not a valid disclaimer of that warranty."
- Sienna Court ¶1 (PDF): "we hold that the purchaser may not." (no IWH claim against a subcontractor with no contract with the purchaser)
- Fattah ¶5 (PDF): first buyer "knowingly, voluntarily, fully and forever," waived the IWH "in exchange for an express warranty." A law-firm note says this pattern "mirror[s] those of many home sales in Illinois" (Faegre Drinker, May 2016, https://www.faegredrinker.com/en/insights/publications/2016/5/residential-builders-prevail-in-illinois-supreme-court-decision-also-benefiting-homebuyers; law-firm; MEDIUM).

Sienna Court also records a municipal-ordinance warranty escrow: Evanston required the developer to fund a "warranty escrow fund" (~$308,000 recovered) (PDF ¶5). Shows local-ordinance protection exists in some towns; none verified for the target counties.

Pending legislation (SEARCH-ONLY, ilga 503/403): **HB 5454, 104th GA, "Protect New Home Buyers"**, sponsor Rep. Dagmara Avelar (co-sponsor reported Natalie Manley), introduced Feb 2026, referred to Rules Committee 2/13/2026; would add a statutory "housing merchant implied warranty" surviving title transfer (reported 1 yr workmanship, 2 yr systems, 6 yr material defects), with exclusion/modification provisions. Title of the Act per search: "Consumer Protection New Construction Residential Housing Act" (unverified whether new or existing). URLs: https://ilga.gov/Legislation/BillStatus?DocNum=5454&GAID=18&DocTypeID=HB&LegId=167349&SessionID=114. Earlier: HB 3499 (2019, "Home Warranty Liability", tabled 4/3/2019). Status after Feb 2026 unknown. Strength MEDIUM (bill existence; contents unverified).

### 1.4 Residential Real Property Disclosure Act (765 ILCS 77)

- Sec. 15 opening (fetch, Onecle copy; version date unknown): "The provisions of this Act do not apply to the following:" ... item (9) "Transfers of newly constructed residential real property that has not been occupied." https://law.onecle.com/illinois/765ilcs77/15.html. Strength: STRONG-but-stale copy.
- SEARCH-ONLY: Public Act 102-0765 text reportedly reads "has never not been occupied" (possible drafting oddity). Net: **builder sales of never-occupied homes are generally outside the disclosure form requirement**, so the statutory seller-disclosure form is not a tool for new-build buyers. Verify current text.

### 1.5 Residential Building Code Act (815 ILCS 670)

SEARCH-ONLY (ilga 503; Justia 403): Sec. 15 says that in a contract for new residential construction in a jurisdiction **without** its own building code, the parties may agree on a code (IRC or a municipal/county code within 100 miles); if not, statutory defaults are read into the contract. Not a lever in the six target counties where municipalities adopt codes. https://ilga.gov/legislation/ilcs/documents/081506700K15.htm. MEDIUM-WEAK (unread).

### 1.6 Condominium and common-interest (developer) rules

- Condo Property Act Sec. 22 (SEARCH-ONLY): seller's failure to make required disclosures lets buyer cancel before closing and recover deposits plus interest; whether there is a private action for post-sale material changes was unsettled (7th Cir. Burke v. 401 N. Wabash, https://caselaw.findlaw.com/court/us-7th-circuit/1627906.html). Escrow-bill attempts HB 3973 (2009-10) and HB 5496 (2011-12) died.
- CICAA (765 ILCS 160/1-50), per Illinois HOA law blog (law-firm, Jan 16, 2025, https://ilhoalaw.com/2025/01/16/765-ilcs-160-1-50-4-things-every-illinois-common-interest-community-association-board-needs-to-know-about-developer-turnover/): "the statute of limitations on claims does not begin to run until the majority of the board" is homeowner-elected (fetch); records turnover within 60 days; "If the developer fails to provide the items within 10 days after the written demand letter is delivered," association may sue (fetch). Daily Herald Q&A (Sept 19, 2020, https://www.dailyherald.com/article/20200919/entlife/200919595): initial board election within 60 days after developer conveys 75% of units or 3 years after recording, whichever is earlier (search summary). MEDIUM (law-firm + secondary; statute unread).

### 1.7 Mechanics liens (770 ILCS 60)

- Law-firm (Illinois Lawyer Now, June 2021): subs on single-family homes give owner preliminary notice within 60 days after work begins; "Any valid mechanic's liens will need to be released before ownership of the property can be transferred." Lien filed within 4 months binds later owners; up to 2 years binds current owner only. https://www.illinoislawyernow.com/2021/06/how-can-mechanics-liens-affect-a-real-estate-transaction/ (fetch). 2025 changes to subcontractor notice delivery effective Jan 1, 2025 (https://www.illinoislawyernow.com/2025/05/illinois-sees-significant-changes-in-2025-for-mechanics-liens/; no specifics). MEDIUM (law-firm; statute unread).
- Regulator example of lien-after-nonpayment pattern: see 1.8 (2006).

### 1.8 Illinois Attorney General actions and complaint reports

| # | Issue | Builder/respondent | Place | Date | Type | URL | Quote | Strength |
|---|---|---|---|---|---|---|---|---|
| a | Suit alleging unfinished new homes and unreturned down payments; warranty not honored | **Alleged:** Lord & Essex, Inc.; Pembrooke Homes LLC; Estates at Brookmere LLC; John J. Popp Jr. (Aurora), Christopher Smith (Peotone) | Brookmere subdivision, Matteson (Cook); Autumn Ridge, Crest Hill (Will) | Sept 3, 2007 | regulator (press release; allegations only, no finding located) | https://illinoisattorneygeneral.gov/News-Room/2006-2018-Press-Archive/200709-04%20Madigan%20Sues%20Cook%20County%20Developers.pdf (PDF read) | "failing to complete construction on 39 homes and by further failing to refund $250,000 in down payments" | STRONG that suit was filed; outcome UNKNOWN (searched, no result) |
| b | Same release: sales agents' oral promises of earlier completion vs 2-year contract; 5% down payment; cancellation riders | same | same | 2007 | regulator | same | "consumers have complained that the defendants extended the completion date on their homes well beyond the promised time frame" | STRONG (as allegations) |
| c | Same release: warranty non-performance | same | same | 2007 | regulator | same | "failed to honor homeowner warranties and to make repairs to items under warranty when requested" | STRONG (as allegation) |
| d | Contractor took deposits on "remodeling or new construction", unpaid subs led to liens | **Alleged:** Robert Yarbrough / Design Construction, Aurora | DuPage County Circuit Ct; Plainfield and Bolingbrook complainants | Mar 2, 2006 | regulator (mostly basement remodels; marginal for new-build) | https://illinoisattorneygeneral.gov/News-Room/2006-2018-Press-Archive/200603-02%20FILES%20SUIT%20AGAINST%20DUPAGE%20CONTRACTOR%20FOR%20LEAVING%20HOMEOWNERS%20WITH%20INCOMPLETE%20WORK%20LIENS%20ON%20THEIR%20PROPERTY.pdf (PDF read) | "failed to pay his suppliers and subcontractors which resulted in liens being placed on some consumers' properties" | STRONG (allegation); relevance MEDIUM-low |
| e | Annual top-10 complaints: Construction/Home Improvement #1; 2,091 complaints in 2023; includes "new construction" in category description | unnamed | Illinois | Mar 5, 2024 | regulator | https://illinoisattorneygeneral.gov/news/story/attorney-general-raoul-recognizes-national-consumer-protection-week-announces-top-10-list-of-consumer-complaints | "ranging from gutter and roof repairs to new construction" (fetch) | STRONG (but category is dominated by repair/remodel; no builder-only count) |
| f | 2024 data: Construction/Home Improvement #1 again, 2,256 complaints; "complete failure by companies to conduct any work after receiving a down payment"; page does not mention "new construction" | unnamed | Illinois | Mar 3, 2025 | regulator | https://illinoisattorneygeneral.gov/news/story/attorney-general-raoul-recognizes-national-consumer-protection-week-announces-top-10-list-of-consumer-complaints-3-3-25 | "the complete failure by companies to conduct any work after receiving a down payment" (fetch) | STRONG |

- **No recent (2019-2026) AG action against a new-home builder located.** Raoul-era suits found concern home-repair/storm/concrete contractors (e.g., May 2022 suit vs two Kane County roofing businesses; https://illinoisattorneygeneral.gov/dA/ec416f339c/202205-03%20FILES%20LAWSUIT%20OVER%20HOME%20REPAIR%20SCAMS%20DEFRAUDING%20DOZENS.pdf, file too large to read, listed in search only).
- Illinois AG joined 18 other states supporting a CFPB limit on mandatory arbitration (per ABC7, Nov 2016; see 2.1).

### 1.9 Consumer-fraud claims against builders (case law, SEARCH-ONLY unless noted)

- Falcon Associates v. Cox, 298 Ill.App.3d 652 (1998): buyers argued a builder's failure to deliver promised insulation (R-19) was fraudulent under the Consumer Fraud Act. https://cite.case.law/ill-app-3d/298/652/ (older, landmark; holdings not verified by me). MEDIUM.
- Olson v. Hunter's Point Homes, LLC, 2012 IL App (5th) 100506: reversed dismissal of ICFA count; intentional-misrepresentation allegations not barred by Moorman doctrine (search summary). MEDIUM. Not Chicago metro (5th Dist.).
- Pack v. Maslikiewicz, 2019 IL App (1st) 182447: ICFA liability affirmed against a rehab-and-resell seller ("trade or commerce" satisfied by buying homes to sell at a profit). MEDIUM. Not a new-build builder.
- Trial-level: Cook County judge found builder liable under ICFA for failing to disclose high water table while rejecting contract/warranty claims (builderonline.com "Chicago Builder Loses Homeowner Suit", https://www.builderonline.com/?p=66581; 403 on fetch; date and builder name not seen). WEAK.
- Statute of limitations/repose, law-firm only (Oct 23, 2023): "statute of limitations for construction defect claims in Illinois is four years" with 10-year repose; section number (reportedly 735 ILCS 5/13-214) not confirmed in that source. https://grzymalalaw.com/how-long-is-a-builder-liable-for-their-work-in-illinois/ (fetch). MEDIUM.

---

## 2. Local complaint evidence (news and public meetings)

Overall: **thin.** No Tribune, Sun-Times, NBC5 Responds, WGN, FOX 32, or Naperville Sun story about named-builder new-build buyer complaints in the six counties was located for 2019-2026. (Tribune and Naperville Sun are blocked from WebSearch.)

| # | Issue | Builder | Place | Date | Type | URL | Quote | Strength |
|---|---|---|---|---|---|---|---|---|
| 2.1 | Mandatory arbitration in builder contract; arbitrator picked from a list supplied by builder's warranty administrator; buyers say they could not choose own arbitrator; leaks, cracked floors reported | **Alleged:** Ryland Homes (acquired by CalAtlantic) | Round Lake (Lake Co.), Huntley (McHenry/Kane), IL; outside target counties but regional | Nov 17, 2016 | major-news (ABC7 I-Team) | https://abc7chicago.com/post/contracts-prevent-new-homeowners-from-suing-over-alleged-shoddy-construction/1611256/ (fetch) | arbitrator chosen "from a list provided by our warranty administrator" (fetch). Builder side: arbitration is "a fair, less costly alternative" (paraphrase) | STRONG for existence of the complaint and clause; allegations unproven |
| 2.2 | Neighbors (not new buyers) complain of construction traffic, debris, standing water at construction sites | Lennar Homes (third builder in subdivision) | Indian Ridge, Minooka (Grundy/Will) | Jul 1, 2019 | local-news (Shaw Local) | https://www.shawlocal.com/2019/07/01/indian-ridge-neighbors-cry-foul-at-minooka-village-board/amxp6mx/ (fetch) | "Our roads were not built to accommodate this weight that's going up and down our streets every day." | MEDIUM-low: single article, complaint is neighbors' not buyers' |
| 2.3 | Builder-produced Chicago-area bankruptcies: deposits/escrow; ~400 customers in limbo | Neumann Homes (Warrenville) | Chicago area | Nov 2007 | trade/major-news aggregation | https://www.builderonline.com/land/neumann-to-finish-homes-return-deposits_o/ (search-only); https://www.wbez.org/eight-forty-eight/2007/10/29/will-neumann-homes-bankruptcy-hurt-housing-market (search-only) | none fetched | MEDIUM (older, landmark) |
| 2.4 | Builder insolvency and buyer deposit priority ($2,425 per person cited) | Kirk Homes | suburban Chicago | Sept 22, 2009 | local-news (Daily Herald) | https://www.dailyherald.com/20090922/business/kirk-homes-reorganization-plan-denied-creditors-discuss-next-steps/ (search-only) | none fetched | MEDIUM (older; search summary only) |
| 2.5 | Drainage/flooding in subdivision: village engineers found missing storm sewer overflows and undersized pipes; annexation agreement HOA never formed | developer unnamed in my view | Mallard Point, Sugar Grove (Kane) | Jan 9, 2010 | local-news (Daily Herald) | https://www.dailyherald.com/20100109/news/sugar-grove-group-fights-flooding-bills/ (search-only; fetch returned empty) | none | WEAK (summary only, 16 yrs old) |
| 2.6 | Suit alleging builders "made promises they didn't deliver" for houses; buyers of 23 homes sued in Will County | **Alleged:** DRH Cambridge Homes / D.R. Horton | Liberty Grove, Plainfield (Will) | **date UNKNOWN** | local-news aggregator snippet | https://api.courthousenews.com/real-estate-63/ (403 on fetch; snippet only; story itself not found in follow-up search) | none verified | WEAK (cannot confirm date or existence of story) |

Not found: village/city board meeting complaints from buyers about named builders in Plainfield, Naperville, Oswego, Yorkville, Aurora, Joliet, Bolingbrook, Romeoville beyond 2.2. Yorkville/Oswego coverage found concerned density and growth opposition (e.g., Kendall County Now, Mar 7, 2025, https://www.shawlocal.com/kendall-county-now/2025/03/07/we-dont-want-to-be-another-oswego-yorkville-residents-oppose-rapid-residential-developments/; not a buyer complaint). School/infra impact fees: none tied to buyer complaints.

Market context only: Lennar reportedly cut suburban asking prices in Plainfield and Algonquin (Hoodline, Dec 2025, https://hoodline.com/2025/12/lennar-quietly-knocks-down-suburban-home-prices-as-chicago-buyers-feel-the-squeeze/; search-only). Price-cut context could feed buyer "price-protection" complaints but none documented.

Windy City Rehab (Chicago Sun-Times, Jan 7, 2020, https://chicago.suntimes.com/news/2020/1/7/21054658/windy-city-rehab-homeowner-lawsuit-full-complaint): renovation/rehab sold in Chicago, not new-build; mentioned in results but not examined. Out of scope.

---

## 3. Forums (reddit blocked; other sites)

**Reddit: not accessible.** No r/chicagosuburbs etc. evidence. Gap for the team to fill manually.

All forum items below are WEAK (single anecdote) unless noted. **Only two items were Illinois-linked.**

| # | Issue | Builder | Place | Date | URL | Quote | Strength |
|---|---|---|---|---|---|---|---|
| 3.1 | Builder demanded proof of liability insurance, then workers' comp, to let an inspector in; poster (an inspector) says this is how to deny access | **Alleged:** Sterling Homes | Chicago area (poster location inferred, "Chicago area" per fetch summary) | Apr 27, 2011 (nachi.org forum) | https://forum.nachi.org/t/builder-obstructs-clients-right-to-inspection/58837 (fetch) | "knows that this is how to deny access for the inspection" (fetch) | WEAK |
| 3.2 | Complaint of poor workmanship (stairs left in rain, basement plumbing leak, cracked 2x4s), repairs took years | **Alleged:** D.R. Horton / Cambridge Homes | Liberty Grove, Plainfield; 2006 purchase | Jan 30, 2010 (ComplaintsBoard; marked "Resolved") | https://www.complaintsboard.com/dr-horton-cambridge-homes-liberty-grove-poor-workmanship-c305251 (fetch) | "Wood stairs were left out in the rain, plumbing in the basement leaked" | WEAK |
| 3.3 | Newer Plainfield reviews of Lennar and Pulte: unresolved items before closing, slow warranty, trim defects; water from grading called "act of God"; Pulte cosmetic-only repair of ceiling crack with underlying soil issue | **Alleged:** Lennar, Pulte | Plainfield | reviews dated through Jul 2026 (ConsumerAffairs, NewHomeSource) | https://www.newhomesource.com/builder/lennar/reviews/644/illinois/chicago-area (403 on fetch); https://www.consumeraffairs.com/homeowners/lennar-homes.html (search-only) | seen in search summary only, not verified | WEAK (reviews; platform moderation unknown) |

Non-Illinois but on-topic anecdotes (do not use as Illinois evidence): nachi.org thread "Are builders allowed to deny 3rd party inspections?" (May 15, 2022) says refusals "uncommon" and builders may require certificates of insurance (https://forum.nachi.org/t/are-builders-allowed-to-deny-3rd-party-inspections/215727); city-data thread (Oct 19, 2011) on builders discouraging private inspections (https://www.city-data.com/forum/real-estate-professionals/1407346-new-construction-pushing-no-private-home.html); city-data closing-delay threads, 2009 and 2015, none Illinois-specific.

Conclusion for forums: Illinois first-hand accounts on closing delays, arbitration, deposits, punch-list refusals, and warranty denial **were not found outside Reddit and review sites**. The only Illinois builder-obstructs-inspection anecdote is 3.1 (2011).

---

## 4. Court cases (Illinois appellate/federal)

| Case | Topic | Place/court | Date | URL | Key text | Strength |
|---|---|---|---|---|---|---|
| Smith v. Jones, 2025 IL App (5th) 231136 | New-home purchase agreement with builder; IWH and workmanship claims; arbitration order reversed because defendants' 2-615/2-619 motions "waived their right to compel arbitration" | Ill. App. 5th Dist. (southern IL) | Feb 18, 2025 | https://www.isba.org/node/96080 (fetch, ISBA summary) | defendants' motions "placed substantive issues before the court and, as a result, waived their right to compel arbitration" | STRONG (court) but secondary summary, outside metro |
| Bain v. Airoom, LLC, 2022 IL App (1st) 211001 | Remodeling (not new build) contract; arbitration clause unconscionable, unenforceable as a whole (no fee-shifting/punitive damages contrary to ICFA) | Ill. App. 1st Dist. (Cook) | May 27, 2022 | https://www.isba.org/node/81047 (fetch) | "several significant portions" of the arbitration agreement were unconscionable | STRONG; relevance to new-build is analogical |
| Petersen; Village Centre; Fattah; Sienna Court | Warranty disclaimer/waiver | Ill. S.Ct. | 1979; 2001; 2016; 2018 | see 1.3 | see 1.3 | STRONG |
| 1324 W. Pratt Condo. Ass'n v. Platt Constr. Group, 2013 IL App (1st) 130744 | Pratt III: IWH against subcontractors where builder insolvent | Ill. App. 1st | 2013 | https://www.lauriebrennan.com/blog/the-illinois-appellate-court-expands-rights-of-homeowners-against-builders-for-latent-defects-in-residential-properties/ (fetch; law-firm) | "the court must look to whether the general contractor is solvent." | Overruled in effect by Sienna Court's overruling of Minton line; do not rely |
| Chinlund v. Heffernan Builders (Ill. App. 2020) | Court vacated judgment that relied on arbitrator's decision | Ill. App. | 2020 | search-only (via lexislegalnews) | not read | WEAK (unread) |
| Fed. N.D. Ill. builder-arbitration decisions | none found | n/a | n/a | n/a | n/a | Gap |

No Illinois appellate decision was found enforcing or striking an arbitration clause in a **builder-vendor new-home purchase contract** other than Smith v. Jones (waiver by litigating). Caution: Illinois enforces arbitration agreements as contracts (search summary citing Carr v. Gateway, 241 Ill.2d 15 (2011)); unconscionability per Bain applies fact by fact.

---

## 5. Builders active in the area: documented complaint patterns (all "alleged")

| Builder | Pattern (alleged) | Place | Date | Source type | Strength |
|---|---|---|---|---|---|
| Lord & Essex / Pembrooke Homes / Estates at Brookmere (Popp, Smith) | Unfinished homes; unreturned $250K deposits; sales-agent promises of earlier completion; unhonored warranties; AG complaint | Matteson (Cook), Crest Hill (Will) | 2007 | regulator allegations | STRONG (suit filed); outcome unknown |
| Ryland Homes (CalAtlantic, now Lennar) | Mandatory arbitration with builder-warranty-administrator list; defects | Round Lake, Huntley | Nov 2016 | major-news | MEDIUM (two cases in one report) |
| Lennar | Neighbors' construction-traffic/debris complaints (Minooka, 2019); buyer reviews of unresolved pre-closing items, grading/water, slow warranty (Plainfield, to Jul 2026) | Minooka; Plainfield | 2019; 2026 | local-news; reviews | WEAK-MEDIUM |
| Pulte | Plainfield buyer reviews: slow repairs; cosmetic fix of soil-related ceiling crack | Plainfield | review sites, c. 2021-2026 | reviews | WEAK |
| D.R. Horton / Cambridge Homes | Liberty Grove Plainfield: 2010 workmanship complaint; unverified Courthouse News snippet of a 23-home Will County suit | Plainfield | 2010; undated | forum/aggregator | WEAK |
| Sterling Homes | Insurance/workers'-comp requirements allegedly used to deny inspector access | Chicago area | Apr 2011 | forum | WEAK |
| Neumann Homes, Kirk Homes | Bankruptcy; deposits and unfinished homes | Chicago metro | 2007; 2009 | trade/local news | MEDIUM (old) |

Insufficient evidence to describe a documented pattern for any builder in Kendall, Kane, DuPage or Grundy counties in 2019-2026.

---

## 6. Gaps (what should be searched next by someone with other access)

1. ilga.gov statute text for: 225 ILCS 441/15-10 full item 30 and repeal date; 765 ILCS 77/15 current wording; 815 ILCS 670/15; HB 5454 text and status; 770 ILCS 60. Also 735 ILCS 5/13-214.
2. Reddit (blocked). Facebook buyer groups. Will County / Kane County / DuPage circuit-court dockets (e.g., Liberty Grove suit; Lord & Essex outcome).
3. Federal N.D. Ill. decisions on builder arbitration (PACER/Westlaw).
4. Village-board minutes (Plainfield, Oswego, Yorkville, Minooka, Joliet) for buyer complaints.
5. Unverified claim to chase: lawkeller.com says warranties "can't be waived or excluded by contract unless explicitly stated"; actual law is waivable under Petersen/Village Centre conditions.
