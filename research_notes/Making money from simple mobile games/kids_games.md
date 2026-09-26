# Making and Monetizing Mobile Games for Young Children (4-7) on iOS / Google Play, 2024-2026

Research scope note: many primary pages (support.google.com, sensortower.com, revenuecat.com, loeb.com, whitecase.com) were blocked by the network proxy during this session, so several findings below come from search-result summaries of those pages rather than full-page reads. They are flagged "(search summary)" where that matters. Apple's App Review Guidelines were read in full.

## 1. Regulation: COPPA (incl. 2025 amendments), UK Age Appropriate Design Code, GDPR-K

### Takeaway
A game for ages 4-7 is clearly "directed to children" under COPPA, so behavioral/targeted ads and profile-building analytics are effectively off the table without verifiable parental consent (VPC); the 2025 amendments (compliance deadline April 22, 2026) add a *separate* consent for disclosing kids' data to third parties/ads, written data-retention and security programs, and wider "directed to children" evidence. In the UK/EU, the Children's Code and GDPR Art. 8 push the same way: high-privacy defaults, profiling and geolocation off, parental consent under 13-16 depending on country. The practical result: the cheapest compliant design is "collect nothing" — no accounts, no third-party ad/analytics SDKs, payments handled by the store behind a parental gate.

### Cited Findings
**COPPA 2025 amendments — timing**
- FTC published final COPPA Rule amendments in the Federal Register on April 22, 2025; effective June 23, 2025; operators must comply by April 22, 2026 (safe-harbor programs have different deadlines) — [Securiti](https://securiti.ai/ftc-coppa-final-rule-amendments/); [Federal Register](https://www.federalregister.gov/documents/2025/04/22/2025-05904/childrens-online-privacy-protection-rule); [Hunton](https://www.hunton.com/privacy-and-information-security-law/ftc-publishes-final-coppa-rule-amendments); [Latham & Watkins](https://www.lw.com/en/insights/ftc-publishes-updates-to-coppa-rule)
- Davis Polk describes FTC "prioritizing COPPA enforcement as new compliance obligations take effect" — [Davis Polk](https://www.davispolk.com/insights/client-update/ftc-prioritizes-coppa-enforcement-new-compliance-obligations-take-effect)
- Note: one search summary stated the amendments "took effect April 22, 2026" — this conflates the effective date (June 23, 2025) with the compliance date (April 22, 2026) — [ppc.land](https://ppc.land/new-coppa-rules-take-effect-june-23-2025-with-major-advertising-changes/)

**COPPA 2025 amendments — substance (search summaries of law-firm analyses)**
- Without separate verifiable parental consent, disclosing children's personal information to third parties for targeted advertising is off-limits (separate consent for third-party disclosure, distinct from consent to collect) — [Loeb & Loeb](https://www.loeb.com/en/insights/publications/2025/05/childrens-online-privacy-in-2025-the-amended-coppa-rule); [ppc.land](https://ppc.land/new-coppa-rules-take-effect-june-23-2025-with-major-advertising-changes/)
- New factors for "directed to children": FTC will consider marketing/promotional materials or plans, representations to consumers or third parties, user or third-party reviews, and the age of users on similar services — [Loeb & Loeb](https://www.loeb.com/en/insights/publications/2025/05/childrens-online-privacy-in-2025-the-amended-coppa-rule); [Fenwick](https://www.fenwick.com/insights/publications/coppas-coming-of-age-key-compliance-changes-in-ftcs-final-rule)
- "Mixed audience" codified: a service directed to children but not primarily targeting them must use a neutral age screen before collecting personal info from any user; users under 13 get full COPPA treatment — [Promise Legal](https://blog.promise.legal/coppa-mixed-age-audience-edtech/); [Loeb & Loeb](https://www.loeb.com/en/insights/publications/2025/05/childrens-online-privacy-in-2025-the-amended-coppa-rule)
- Other changes covered in firm alerts (written information-security program, written data-retention policy, expanded definition of personal info incl. biometrics) — [Securiti](https://securiti.ai/ftc-coppa-final-rule-amendments/); [Gibson Dunn PDF](https://www.gibsondunn.com/wp-content/uploads/2025/01/ftc-updates-to-coppa-rule-impose-new-compliance-obligations-for-online-services-that-collect-data-from-children.pdf) (not fetched in full; details should be verified there)

**Analytics / persistent identifiers**
- "Support for internal operations" exception: a persistent identifier (without other PI) may be collected without consent only for narrow purposes — site/service functionality, network communications, authentication, serving *contextual* ads, security, legal compliance, fulfilling a child's specific request — [Promise Legal via search](https://blog.promise.legal/startup-central/coppa-compliance-in-2025-a-practical-guide-for-tech-edtech-and-kids-apps/); [FTC COPPA FAQ](https://www.ftc.gov/business-guidance/resources/complying-coppa-frequently-asked-questions)
- Profile-building (analytics SDKs that aggregate per-user event profiles, recommendation engines, ML) and behavioral advertising fall outside the exception and need VPC — [Promise Legal](https://blog.promise.legal/startup-central/coppa-compliance-in-2025-a-practical-guide-for-tech-edtech-and-kids-apps/)

**Penalties / enforcement**
- Civil penalties up to $53,088 per violation (2025 inflation-adjusted) — [FTC COPPA FAQ](https://www.ftc.gov/business-guidance/resources/complying-coppa-frequently-asked-questions); [LegalClarity](https://legalclarity.org/list-of-ftc-fines-statutory-limits-and-civil-penalties/)
- Epic Games: $520M (2022, COPPA + Section 5); a game developer paid $20M on Jan 17, 2025 over loot-box practices (COPPA + Section 5); toy maker Apitor $500K penalty (suspended for inability to pay) — [Mintz](https://www.mintz.com/insights-center/viewpoints/2826/2025-09-05-ftc-coppa-enforcement-still-alive-and-well); [ReedSmith](https://www.reedsmith.com/our-insights/blogs/viewpoints/102l3cw/its-all-about-the-kids-the-ftcs-latest-round-of-coppa-enforcement/)

**UK Age Appropriate Design Code (Children's Code)**
- Applies to apps, games, connected toys likely to be accessed by children; enforced by the ICO under Data Protection Act 2018 — [ICO](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/childrens-information/childrens-code-guidance-and-resources/age-appropriate-design-a-code-of-practice-for-online-services/)
- Requirements: high-privacy settings by default; geolocation off by default; profiling off by default unless a compelling reason in the child's best interest; no nudge techniques to get kids to share data or weaken privacy — [Evalian](https://evalian.co.uk/childrens-code/); [TrustArc](https://trustarc.com/resource/uk-age-appropriate-design-code/)
- Note the UK/EU test is "likely to be accessed by children," broader than COPPA's "directed to children" (standard Code scope; see ICO link above).

**GDPR-K (Art. 8)**
- Consent-based processing of a child's data for an online service offered directly to them requires parental consent below 16, which member states may lower to no less than 13 — [GDPR-info Art. 8](https://gdpr-info.eu/art-8-gdpr/)
- Ages vary: 16 (Germany, Netherlands, Hungary, Lithuania, Luxembourg, Slovakia); 15 (France); 14 (Austria); 13 (UK, Spain, Ireland, Denmark, Sweden, Poland, Czechia, Latvia) — [GDPR Local](https://gdprlocal.com/digital-age-of-consent-under-the-gdpr/); [EuConsent](https://euconsent.eu/digital-age-of-consent-under-the-gdpr/)

### Inferences
- For a 4-7 app, every user is under 13 everywhere, so ad-funded models collapse to contextual-only ads and analytics must be first-party/aggregate or a kids-certified vendor. A "no data collected" app with store-handled IAP/subscriptions avoids VPC entirely, which is why most premium kids brands operate this way.
- The new "marketing materials / reviews / similar services' audience" factors make it harder to label a cartoon-character game "general audience" if it is marketed via a children's book.

### Gaps
- Could not fetch the full text of the 2025 amendments or firm analyses (proxy blocks); exact wording on data-retention and security-program obligations and the requirement to disclose internal-operations uses of persistent identifiers in the notice should be verified in the [Federal Register](https://www.federalregister.gov/documents/2025/04/22/2025-05904/childrens-online-privacy-protection-rule).
- Did not research US state laws (e.g., California AADC litigation, app-store age-verification laws in Utah/Texas) that may add obligations in 2026.

## 2. Apple Kids Category (1.3, 5.1.4) and Google Play Families / Teacher Approved / Self-Certified Ads SDKs

### Takeaway
Apple's Kids Category bans links out, purchases and "distractions" outside a parental gate, bans sending PII or device info to third parties, and bans third-party analytics/ads except narrow exceptions (no IDFA or identifying data; contextual ads only from vendors with human-reviewed creatives). Google Play's Families policy lets child-audience apps show ads only via Families Self-Certified Ads SDK versions, and the Kids tab surfaces only Teacher Approved apps, which is the main organic discovery lever on Android.

### Cited Findings
**Apple (read directly)**
- 1.3: Kids Category apps "must not include links out of the app, purchasing opportunities, or other distractions to kids unless reserved for a designated area behind a parental gate." Once in the category, updates must keep meeting the rules even if you deselect it — [Apple App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
- 1.3: "Kids Category apps may not send personally identifiable information or device information to third parties. Apps in the Kids Category should not include third-party analytics or third-party advertising." Limited exceptions: third-party analytics that don't collect/transmit IDFA or any identifiable info about children, location or devices; third-party *contextual* ads from services with publicly documented Kids practices incl. human review of ad creatives — [Apple](https://developer.apple.com/app-store/review/guidelines/)
- 5.1.4(a): apps may ask for birthdate and parental contact only to comply with statutes; "Apps intended primarily for kids should not include third-party analytics or third-party advertising" — this applies even outside the Kids Category — [Apple](https://developer.apple.com/app-store/review/guidelines/)
- 5.1.4(b): Kids Category or any app collecting PI from minors needs a privacy policy; the parental gate "is generally not the same as securing parental consent to collect personal data" under privacy statutes — [Apple](https://developer.apple.com/app-store/review/guidelines/)
- Apple's Kids Category announcement: parents expect data protection, age-appropriate content, parental gates, human-reviewed ads — [Apple Developer News](https://developer.apple.com/news/?id=091202019a)

**Google Play (search summaries; support pages blocked)**
- If target audience is only children, only self-certified ads SDK versions may be used; if audience includes children and older users, ads shown to children must come only from self-certified SDKs (e.g., via neutral age screen) — [Play Console Help: Families Self-Certified Ads SDK Program](https://support.google.com/googleplay/android-developer/answer/12955712)
- Developer remains responsible for all SDKs' compliance even if self-certified — [Families Self-Certified Ads SDK Policy](https://support.google.com/googleplay/android-developer/answer/12918983?hl=en)
- Families policy and data-practices pages (AAID and identifier restrictions for child audiences) — [Families Policies](https://support.google.com/googleplay/android-developer/answer/9893335?hl=en); [Data practices in Families apps](https://support.google.com/googleplay/android-developer/answer/11043825?hl=en); a "Preview: Google Play Families Policies" page exists, suggesting updates in progress — [Preview](https://support.google.com/googleplay/android-developer/answer/17122218)
- AdMob supports tagging ad requests for child-directed treatment — [AdMob Help](https://support.google.com/admob/answer/6219315?hl=en)
- Teacher Approved (since 2020): apps reviewed by teachers/child-development specialists (panel of 200+ US teachers) on design, appeal, enrichment, age appropriateness, ads, IAP and cross-promotion; must first meet Designed for Families requirements; all apps in the Kids tab are Teacher Approved — [TechCrunch](https://techcrunch.com/2020/04/15/google-play-adds-a-teacher-approved-section-to-its-app-store/); [Android Developers Blog](https://android-developers.googleblog.com/2022/11/helping-kids-and-families-find-high-quality-apps-for-kids.html); [Play Console Teacher Approved](https://play.google.com/console/about/programs/teacherapproved/)

### Inferences
- On iOS, a 4-7 game realistically ships with zero third-party ad SDKs and either no analytics or a privacy-minimal one; purchases/subscription paywall sit behind a parental gate (adult-only math/reading challenge).
- Teacher Approved rewards low ads/IAP pressure, so an ad-heavy kids game both earns little and loses the main Android discovery surface.

### Gaps
- Could not read the current Families policy text or the current self-certified SDK list (proxy block). Whether the SDK application window reopened in 2025 was not confirmed.

## 3. Business models that work for kids apps, with revenue numbers and trends

### Takeaway
The market has consolidated from $1-3 premium one-off apps (Toca Boca's original model) to (a) subscription "worlds" with hard paywalls + free trial (Sago Mini World, Pok Pok, Lingokids, Toca's Piknik), (b) free-to-play hubs with parent-purchased content packs (Toca Boca World), (c) free nonprofit (Khan Academy Kids), and (d) curated platforms (Apple Arcade, and since April 2026 Netflix Playground, which is built around licensed IP). Ad-supported kids games earn a fraction of general-audience eCPMs.

### Cited Findings
**Toca Boca / Spin Master**
- Toca Boca historically charged $0.99-$2.99 per app with few free apps — [TechCrunch 2013 via search](https://techcrunch.com/2013/03/06/kids-app-maker-toca-boca-expands-with-zinc-roe-acquisition-sets-up-studio-in-toronto)
- Standalone Toca Life apps removed from App Store/Google Play in Jan 2024 (Amazon June 30, 2024), consolidated into free-to-play Toca Boca World with IAP; Oct 2023 older titles merged into Toca Boca Jr under the Piknik preschool subscription — [Wikipedia: Toca Boca](https://en.wikipedia.org/wiki/Toca_Boca)
- Piknik pricing: Toca Boca Jr plan $7.99, Piknik Unlimited $11.99/month (varies by region) — [Wikipedia: Toca Boca](https://en.wikipedia.org/wiki/Toca_Boca) (search summary)
- Toca Boca World MAU ~54M in Q2 2025 (-5% YoY); Spin Master Digital Games revenue $46.3M in Q2 2025 (+33.4%), $51.5M in Q3 2025, $53.4M in Q4 2025; ~479K subscriptions across digital properties in Q2 2025 (+12%); ~70M MAU (Q3) and ~60M (Q4) across Toca Boca + Piknik — [Investing.com Q2 2025](https://www.investing.com/news/company-news/spin-master-q2-2025-slides-digital-games-shine-amid-overall-revenue-decline-93CH-4162781); [Spin Master Q3 2025](https://www.prnewswire.com/news-releases/spin-master-reports-q3-2025-financial-results-302599078.html); [Spin Master Q4 2025](https://www.prnewswire.com/news-releases/spin-master-reports-q4-2025-financial-results-302704794.html). Note: Digital Games segment also includes other titles (e.g., PAW Patrol games), so not all is Toca.

**Subscriptions**
- Sago Mini World (Piknik/Spin Master): Sensor Tower estimate ~100K downloads and ~$600K revenue in a recent month (US App Store page, date unspecified) — [Sensor Tower](https://app.sensortower.com/overview/874425722?country=US) (search summary)
- Lingokids: US weekly revenue $253K-$293K in Q2 2024 (toddler games); iOS US peak ~$409K/week in Feb 2025; recent estimate ~500K downloads and ~$3M/month — [Sensor Tower Q2 2024 toddlers](https://sensortower.com/blog/2024-q2-unified-top-5-toddlers%20games-revenue-us-642b50fae1714cfff1ccbece); [Sensor Tower iOS Q1 2025](https://sensortower.com/blog/2025-q1-ios-top-5-educational%20games-revenue-us-642f2824e1714cfff1ed8590); [Sensor Tower app page](https://app.sensortower.com/overview/1002043426?country=US) (search summaries)
- Pok Pok: Apple Design Award winner; founded 2019 by Melissa Cash (ex-Disney) and Esther Huybreghts; 9x subscriber growth in one year, >1M downloads, MRR +350% YoY; >$10M VC incl. $6M Series A; TIME100 Most Influential Companies 2025 — [startupintros](https://startupintros.com/orgs/pok-pok); [TIME](https://time.com/collections/time100-companies-2025/7289651/pok-pok/); [Sub Club podcast](https://subclub.com/episode/why-more-apps-need-to-be-more-than-just-apps-melissa-cash-felix-boudreau-pok-pok)
- Pok Pok uses a hard paywall at the start plus free trial so the child can try it; RevenueCat argues hard paywalls suit kids apps because parents want no upsells during play; relentless paywall testing — [RevenueCat blog](https://www.revenuecat.com/blog/growth/whats-the-best-way-to-monetize-kids-apps/) (search summary)

**Free / nonprofit**
- Duck Duck Moose donated its IP to Khan Academy in Aug 2016 (for $1 legal formality); all 21 apps made free; its team built Khan Academy Kids — [EdSurge](https://www.edsurge.com/news/2016-08-27-khan-academy-buys-children-s-app-developer-duck-duck-moose-for-1); [TechCrunch](https://techcrunch.com/2016/08/26/kids-app-maker-duck-duck-moose-joins-khan-academy/)

**Platforms**
- Netflix Playground launched April 6, 2026 (US, CA, UK, AU, PH, NZ; worldwide April 28): standalone games app for kids 8 and under, included with Netflix, no ads/IAP, built on licensed IP (Peppa Pig, Sesame Street, Dr. Seuss) — [MacRumors](https://www.macrumors.com/2026/04/06/netflix-playground-kids-app/); [About Netflix](http://about.netflix.com/en/news/netflix-expands-kids-entertainment-lineup-with-playground-app-for-games); [Hollywood Reporter](https://www.hollywoodreporter.com/business/business-news/netflix-launches-games-app-kids-1236556431/)
- Apple Arcade: $6.99/month, 200+ titles, no ads or IAP — [The Next Web](https://thenextweb.com/news/netflix-playground-kids-games-app)

**Ads in kids apps**
- eCPMs on COPPA traffic are 2.5x to >5x lower than non-COPPA traffic; the kid ad-monetization "island" is shrinking in 2026 — [GameBiz Consulting](https://www.gamebizconsulting.com/newsletter/admon-newsletter-11-the-shrinking-island-ad-monetization-underage-users); [GameBiz ethics guide](https://www.gamebizconsulting.com/blog/ad-monetization-in-kids-games-and-apps-how-to-do-it-right)
- Analogous data point: YouTube "made for kids" content earns ~$1-3 RPM because only contextual ads serve — [vidIQ](https://vidiq.com/blog/post/make-money-kids-youtube-channel/)

### Inferences
- Revenue in kids apps is concentrated in a few subscription brands earning $0.5-3M+/month; the model depends on a large content library (to justify a recurring fee) and paid acquisition — hard for a single-game indie.
- For a small developer with one character, a one-time premium price or a "free lite + one-time full unlock" behind a parental gate is the most compatible model; a subscription only makes sense once there is a library.
- Licensed-IP demand from Netflix Playground/Arcade is for big brands; a new book IP is unlikely to be pitched successfully without an audience.

### Gaps
- No verified Sago Mini World subscriber count, Pok Pok absolute revenue, or Khan Kids usage figures; Sensor Tower estimates are model-based and dates unclear.
- No data on Apple Arcade/Netflix developer deal sizes for kids titles.

## 4. Indie kids app makers: realistic revenue and discovery

### Takeaway
I found no credible, detailed 2024-2026 postmortem from an indie kids-app studio with revenue numbers. General indie-app data is sobering: RevenueCat's 2026 report puts the median subscription app at <$50/month after 12 months, with only 17.2% reaching $1K/month and 3.5% reaching $10K/month. Kids discovery depends on App Store Kids editorial / awards, Google's Teacher Approved Kids tab, parent/teacher word of mouth and review sites; paid UA is how the big subscription brands grow.

### Cited Findings
- Median subscription app revenue after 12 months <$50/month; 17.2% reach $1K/month; 3.5% reach $10K/month — [RevenueCat State of Subscription Apps 2026](https://www.revenuecat.com/blog/growth/subscription-app-trends-benchmarks-2026) (search summary)
- One indie developer earned $2,865 total across three years of multiple app launches — [Atterdag Apps](https://atterdagapps.com/posts/3-years-as-indie-dev/)
- Kids-app monetization: paid, freemium and "paymium" can all work; soft monetization approach recommended — [SlideShare kids apps deck](https://www.slideshare.net/slideshow/cc-slides-for-slideshare/16530962) (older, low-authority)
- Teacher Approved badge/Kids tab is the gated Android discovery route — [Android Developers Blog](https://android-developers.googleblog.com/2022/11/helping-kids-and-families-find-high-quality-apps-for-kids.html); example indie that publicized its badge: [STEM Buddies](https://www.stem-buddies.com/post/stem-buddies-is-teacher-approved-by-google-play)
- Pok Pok's growth marketing emphasizes creative testing and agility (paid growth) — [Bidease interview](https://www.bidease.com/blog/felix-boudreau-pok-pok-growth-tips)

### Inferences
- Realistic baseline for a single indie kids game with no marketing: hundreds to low thousands of dollars total; upside mostly comes from an Apple feature, Teacher Approved placement, or leveraging an existing audience (book readers, schools, libraries).
- Ad-free/privacy-first design is itself a marketing asset with parents and teachers.

### Gaps
- No verified indie kids-game postmortems with numbers (2024-2026). Kidscreen and PocketGamer.biz pieces were not reached.

## 5. Book/character IP extensions into apps

### Takeaway
Big licensed preschool brands do earn meaningful app revenue (World of Peppa Pig ~$500K/month est.), and book brands (Pete the Cat, Dr. Seuss) keep getting apps — but their value comes from pre-existing mass awareness (TV, billions in retail). A book-only character without broad recognition gets little lift from the IP itself.

### Cited Findings
- World of Peppa Pig app: ~$500K estimated monthly revenue and ~100K downloads in Nov 2023 (Sensor Tower) — [Sensor Tower](https://app.sensortower.com/ios/us/entertainment-one/app/world-of-peppa-pig/1175384784) (search summary)
- Peppa Pig brand generated ~$1.35B global retail sales in 2019 — [Statista](https://www.statista.com/statistics/623382/retail-revenue-peppa-pig/)
- Pete the Cat has multiple apps, incl. "Pete the Cat: School Jam" and new "Pete The Cat: Groovy Games" (educational mini-games: puzzles, patterns, numbers, matching) — [App Store](https://apps.apple.com/us/app/pete-the-cat-groovy-games/id6752550589); [Apptopia](https://apptopia.com/ios/app/520299922/about)
- Dr. Seuss, Peppa Pig and Sesame Street IP now distributed via Netflix Playground — [MacRumors](https://www.macrumors.com/2026/04/06/netflix-playground-kids-app/)

### Inferences
- For "Mr. Not Fair," the app's value is more likely as a brand-extension/marketing channel for the book (and vice versa) than as a standalone profit center — e.g., a low-price companion game promoted inside the book, at readings, and to teachers (fairness/emotions theme fits SEL classroom use).

### Gaps
- No revenue data found for Pinkalicious, Mo Willems, or Pete the Cat apps; no data on "Mr. Not Fair" audience size.

## 6. Would a general-audience casual game using a child character be "directed to children"?

### Takeaway
Possibly. COPPA uses a totality-of-circumstances test; animated characters, child-oriented activities, bright visuals, music, and — since 2025 — marketing materials, reviews, and the audience of similar services all count. A character from a children's picture book, marketed to that book's readers, pushes strongly toward "directed to children" or at least "mixed audience" (requiring a neutral age screen and COPPA treatment of under-13s). Both stores also judge by target audience/content.

### Cited Findings
- FTC factors: subject matter, visual content, animated characters or child-oriented activities, music/audio, age of models, child celebrities, advertising on/promoting the service, empirical audience evidence; no single factor dispositive — [FTC COPPA FAQ](https://www.ftc.gov/business-guidance/resources/complying-coppa-frequently-asked-questions)
- FTC recognizes some animated characters are directed to a general audience; but traditionally child-oriented activities (dress-up, playing with toys) indicate child-directedness — [FTC COPPA FAQ](https://www.ftc.gov/business-guidance/resources/complying-coppa-frequently-asked-questions); [FTC YouTube guidance](https://www.ftc.gov/business-guidance/blog/2019/11/youtube-channel-owners-your-content-directed-children)
- 2025 rule adds marketing/promotional plans, representations, reviews, and similar services' audience ages as evidence — [Loeb & Loeb](https://www.loeb.com/en/insights/publications/2025/05/childrens-online-privacy-in-2025-the-amended-coppa-rule)
- Mixed-audience services must age-screen before collecting PI — [Promise Legal](https://blog.promise.legal/coppa-mixed-age-audience-actual-knowledge/)
- Google: if target audience includes children and older users, ads to children must come only from self-certified SDKs (e.g., via neutral age screen) — [Play Console Help](https://support.google.com/googleplay/android-developer/answer/12955712)

### Inferences
- A general-audience casual game (ad-monetized, e.g., hybrid-casual with rewarded video) featuring Mr. Not Fair would need to deliberately avoid kid-coded design and marketing, or else run a neutral age gate and serve only contextual/certified ads to under-13s — cutting into the ad eCPM advantage that makes general casual games attractive.
- Money-bet comparison: a general-audience casual game has higher theoretical ceiling (full ad eCPMs 2.5-5x+ kids' levels) but is a hits business dominated by paid UA, and using a picture-book character undermines the "general audience" claim. A kids game has lower ceilings and strict rules but lower competition for a niche, fits the IP, and can cross-promote the book. For a small developer the lower-risk path is a small, ad-free, premium or one-time-unlock kids game tied to the book, with modest revenue expectations; a separate general-audience casual game should use a non-child-coded concept if the goal is ad revenue.

### Gaps
- No FTC enforcement example specifically about a general-audience mobile game featuring a book character; legal advice needed for the specific design.
