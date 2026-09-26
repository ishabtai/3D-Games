# Monetization Economics of Simple Mobile Games (Hypercasual / Hybrid-Casual / Casual Puzzle), 2024-2026

> Method note: WebFetch was blocked by the network proxy for most domains (tenjin.com, udonis, gamigion), so the findings below come from search-result extracts of the cited pages, not full-page reads. Figures from secondary blogs (gamegrowthadvisor.com, maf.ad, udonis, cas.ai, etc.) are aggregations; treat them as indicative. Primary data providers are Sensor Tower, AppMagic, GameAnalytics, Tenjin/CAS, Appodeal and Liftoff.

## 1. Revenue models: which dominate by segment, and the hypercasual → hybrid-casual shift

### Takeaway
Hypercasual is ads-only (mostly interstitial plus rewarded) and has been collapsing since 2022 as CPIs rose after ATT; the money moved to hybrid-casual (ads plus IAP, with IAP growing fastest) and to IAP-led puzzle (match-3). Pure ad-monetized block puzzles are the exception: Block Blast shows a pure-IAA puzzle can still reach enormous scale because its retention is so high.

### Cited Findings
- Hybridcasual IAP revenue grew 37% YoY in 2024 (Sensor Tower State of Mobile Gaming 2025). Mobile game IAP overall rose 4% to $80.9bn in 2024, the first YoY growth since 2021. — [Sensor Tower State of Mobile Gaming 2025](https://sensortower.com/blog/state-of-mobile-gaming-2025)
- Sensor Tower's 2024 report (on 2023) noted about 30% growth in hybridcasual revenue. — [Game World Observer](https://gameworldobserver.com/2024/04/08/state-of-mobile-gaming-2024-sensor-tower-report)
- AppMagic Casual Report 2025: since 2024, Sort and Screw puzzles each doubled their IAP revenue and **Block Puzzles grew about 10x YoY** in IAP. — [AppMagic Casual Report 2025](https://appmagic.rocks/research/casual-report-2025)
- AppMagic H1 2025: three genres generate about 80% of casual revenue. AppMagic's Q1 2025 hybridcasual top 10 was dubbed "The Great Puzzle Takeover". — [AppMagic H1 2025](https://appmagic.rocks/research/casual-report-h1-2025); [AppMagic Q1 2025 hybridcasual](https://appmagic.rocks/blog/hybridcasual-q1-2025/?hl=en)
- Sensor Tower's State of Gaming 2026 puts the hybrid-casual lifestyle/puzzle revenue mix at **59% IAP / 41% in-app advertising**, as cited by a secondary blog. — [Game Growth Advisor](https://gamegrowthadvisor.com/blog/2026-04-16-hybrid-casual-game-design-strategy-2026/)
- Hypercasual installs fell 14% in 2023. — [maf.ad (aggregator)](https://maf.ad/en/blog/mobile-gaming-statistics/); see also [PocketGamer.biz "What happened to hypercasual?"](https://www.pocketgamer.biz/what-happened-to-hypercasual-the-markets-evolution-over-the-past-year/)
- Voodoo's hypercasual business faced margin pressure from copycats, rising CPI and ad-load saturation, with EBITDA below 13% in 2021 (older data). ATT/IDFA raised UA costs and cut ad-inventory value. — [Sacra on Voodoo](https://sacra.com/c/voodoo/)
- Voodoo went from $0 to $250M in hybridcasual revenue in 3 years (as of mid-2024). — [Deconstructor of Fun](https://www.deconstructoroffun.com/blog/2024/6/3/voodoos-secret-sauce-from-0-to-250m-hybridcasual-revenue-in-3-years). Voodoo's hybrid-casual bar is about 15% D7 retention, and it kills titles fast (2023). — [Game World Observer](https://gameworldobserver.com/2023/07/25/voodoo-hybrid-games-d7-retention-games-and-names-podcast)
- A 2026 summary reports that Voodoo moved its teams off hypercasual entirely, with CEO Alexandre Yazdi writing in March 2026 that the model of launching new games to offset old ones' decline "was no longer viable". This comes from a secondary source; I could not verify the primary statement. — [Voodoo / Innovecs summary via search](https://www.innovecsgames.com/blog/hyper-casual-games/)
- Royal Match reached the top of the puzzle charts with no in-game ads, monetizing purely through IAP. — [CAS.ai hybrid monetization guide](https://cas.ai/blog/hybrid-monetization-in-mobile-games-a-practical-guide/)
- Logic/puzzle games often run about 30% ads / 70% IAP, leaning on rewarded ads and banners rather than interstitials. — [CAS.ai](https://cas.ai/2025/10/09/hybrid-monetization-mobile-games-guide-2-2-2-8-2-2-2-8-3-3-4-5-6-7/)
- Ultracasual puzzle examples that are ad-heavy: Cookingdom (ABI Games, launched March 2025) had 830k DAU and an estimated $43k–55k/day in ad revenue. Color Block Jam made about $150k/day. Dreamy Room (cozy puzzle) made about $80k/day, 89% from ads. — [Felix Braberg, Mobile Ad Revenue newsletter](https://felixbraberg.substack.com/p/the-mobile-ad-monetization-newsletter-57a); [Color Block Jam](https://felixbraberg.substack.com/p/unlocking-the-secrets-of-color-block-71d); [Dreamy Room](https://felixbraberg.substack.com/p/we-played-dreamy-room-its-brilliant-50d)
- Subscriptions and battle passes: I found no puzzle-specific 2024-26 data on subscriptions or passes. Royal Match and Candy Crush both use season or pass-style events, but I have no source for their revenue share.

### Inferences
- Segment-dominant models:
  - **Hypercasual**: interstitial plus rewarded, near-100% ads.
  - **Hybrid-casual**: rewarded plus interstitial plus IAP (remove-ads, boosters, coins, sometimes passes), trending toward roughly a 60/40 IAP/ads mix.
  - **Match-3 at the top**: overwhelmingly IAP (Royal Match has no ads).
  - **Block puzzle / sudoku-likes**: mostly ads (Block Blast ~100% ads, Woodoku ~74% ads).
- For a solo dev, a block or logic puzzle with ads-first monetization plus a remove-ads IAP matches what actually works in the subgenre.

### Gaps
- No verified Sensor Tower primary numbers for the "59/41" split. It came through a secondary blog.
- No subscription or battle-pass revenue-share data specific to casual puzzle.

## 2. Benchmarks: eCPM, ARPDAU, retention, LTV, conversion, ad/IAP split

### Takeaway
US rewarded video runs about $15–20 eCPM and interstitial about $11–14. Emerging markets are a fraction of that. Hypercasual ARPDAU is only about $0.03–0.08, versus about $0.15–0.50 for hybrid-casual. Median D1 retention is about 22% and median D7 about 4%. Only about 1.5–5% of players ever pay.

### Cited Findings
**eCPM**
- US rewarded video eCPM: **$19.63 iOS, $16.49 Android**, $15.15 blended. UAE ($14.55) and Australia ($13.80) follow. — [Search extract of Tenjin/CAS Ad Monetization Benchmark 2026 (updated Aug 13, 2026 with Q2 2026 data)](https://tenjin.com/blog/ad-mon-gaming-2026/); [Maf.ad eCPM](https://maf.ad/en/blog/mobile-ads-ecpm/)
- Interstitial eCPM: North America about **$9.70 Android and $13.60 iOS**. The US country-level figure is $12.65 blended, and US Android is $11.06. — [Tenjin 2026 via search](https://tenjin.com/blog/ad-mon-gaming-2026/); [Mistplay](https://business.mistplay.com/resources/mobile-ads-ecpm)
- Rewarded video has the highest eCPM globally on both platforms. Banners are far lower than both full-screen formats. The global average for rewarded is in the "high single digits to low double digits". India's interstitial eCPM is trending up, and Brazil is climbing among emerging markets. — [Tenjin 2026](https://tenjin.com/blog/ad-mon-gaming-2026/); [Appodeal Benchmarks](https://appodeal.com/blog/mobile-ecpm-report-app-ad-monetization-worldwide-performance/)
- The Tenjin 2025 edition and the Q2 2024 edition also exist, for trend comparison. — [Tenjin 2025](https://tenjin.com/blog/ad-monetization-benchmark-report-2025-ecpm-ad-revenue/); [Tenjin Q2'24 summary](https://gamedevreports.substack.com/p/tenjin-ad-monetization-in-mobile-00b)

**ARPDAU / ARPU**
- Blended ARPDAU is about **$0.15–0.50 for hybrid-casual** versus **$0.03–0.08 for hypercasual**. — [Game Growth Advisor KPIs 2026 (aggregator)](https://gamegrowthadvisor.com/blog/2026-03-17-mobile-game-kpis-benchmarks-2026/); [Playio ARPDAU](https://blog.playio.co/arpdau-benchmarks-mobile-games)
- Puzzle ARPU is about $0.20–0.60, with payer conversion around 1.8%. — [MAF conversion benchmarks (aggregator)](https://maf.ad/en/blog/mobile-game-conversion-rates/)

**Retention (GameAnalytics 2025/2026, 11,600 games, 1.48B MAU)**
- Median **D1 about 22%**, top 25% just above **30%**. Median **D7 just under 4%**, top 25% about **6–7%**. Puzzle is among the strongest genres for mid- and long-term retention. — [GameAnalytics 2026 Benchmarks](https://www.gameanalytics.com/reports/2026-mobile-pc-gaming-benchmarks); [GameDevReports summary](https://gamedevreports.substack.com/p/gameanalytics-mobile-and-pc-game)
- Hybrid-casual targets are about **D7 20% / D30 10%**, while hypercasual D30 is near zero. This comes from an aggregator and reflects successful titles, not the median. — [Game Growth Advisor](https://gamegrowthadvisor.com/blog/2026-04-16-hybrid-casual-game-design-strategy-2026/)
- Voodoo's greenlight bar for hybrid-casual is about 15% D7 (2023). — [Game World Observer](https://gameworldobserver.com/2023/07/25/voodoo-hybrid-games-d7-retention-games-and-names-podcast)

**IAP conversion**
- 2–5% of casual players convert monthly. The average across mobile games is 1.5–3.5% of actives purchasing (2026). — [Udonis on Medium](https://medium.com/udonis/how-to-improve-conversion-rate-in-mobile-games-624a969edc3d); [MAF](https://maf.ad/en/blog/mobile-game-conversion-rates/)

**CPI / ROAS (UA side of unit economics)**
- Puzzle CPI on iOS is about $3.00. Hybrid-casual Android global CPI nearly doubled, from $0.54 (2024) to $0.95 (2025). Western iOS casual CPI rose about 38% YoY. North America gaming CPI rose 31% to $1.68 (US $1.71) in 2025. Puzzle D7 ROAS is about 6.9%. iOS delivers more than 2x the D30 ROAS of Android in most genres. — [Liftoff 2025 Casual Gaming Apps Report](https://liftoff.ai/2025-casual-gaming-apps-report/); [Liftoff highlights](https://liftoff.ai/blog/highlights-2025-casual-gaming-apps-report/); [Udonis casual CPIs](https://www.blog.udonis.co/mobile-marketing/mobile-games/casual-games)
- Blended gaming CPI reached about $0.56 in 2026, up 30% in a year. — [Innovecs (secondary)](https://www.innovecsgames.com/blog/hyper-casual-games/)

**Ad vs IAP split, puzzle**
- Woodoku is about 26% IAP / 74% ads (AppGoblin estimate). Block Blast is almost 100% ads. Dreamy Room is 89% ads. Hybrid-casual puzzle overall is about 59% IAP / 41% ads. Logic/puzzle is about 30% ads / 70% IAP. See the sections above and below for sources.

### Inferences
- A rough per-DAU revenue check for an ad-only puzzle: about 5–10 rewarded/interstitial impressions per DAU per day at a blended ~$3–8 global eCPM works out to roughly $0.015–0.08 ARPDAU. That is consistent with the hypercasual range and with Block Blast's implied ~$0.01 (see section 3).
- With hybrid-casual CPIs of about $1–3 and ARPDAU of $0.03–0.08, paid UA almost never pays back for an ads-only solo game. Organic, ASO or viral growth is the realistic path for a solo developer.

### Gaps
- Could not retrieve exact tier-3 (India, Indonesia, Brazil) rewarded eCPM values. Tenjin, Appodeal and Liftoff pages were not fetchable. Direction only: much lower than the US.
- No authoritative 2024-26 LTV benchmark by subgenre. Sources say LTV is "harder to benchmark publicly".
- No 2024-26 D30 median from GameAnalytics was captured.

## 3. Case studies: Block Blast, Woodoku, Royal Match, Candy Crush, solo devs

### Takeaway
Block Blast (Hungry Studio) is the defining 2024-25 story. It is a pure-ad block puzzle that reached about 70M DAU and 300M MAU, with an estimated ~$17.5M/month in ad revenue, yet IAP is negligible. Royal Match and Candy Crush each gross over $1B/year in IAP. I found no verifiable 2024-26 solo-developer puzzle postmortems with numbers.

### Cited Findings
**Block Blast (Hungry Studio)**
- Hungry Studio was founded in 2021, according to one source. Xiaomi founder Lei Jun invested in 2020 (about 5.8% stake) and exited in 2023. There is a date inconsistency between the sources here. — [Playgama](https://playgama.com/blog/game-faqs/who-owns-and-developed-block-blast-game/); [36Kr (Tencent invests in Hungry Studio)](https://eu.36kr.com/en/p/3706617203732616)
- 40M DAU / 160M MAU in December 2024, rising to **70M DAU / 300M MAU**. It was **the #1 game worldwide by downloads in 2025**. — [Mobilegamer.biz data digest](https://mobilegamer.biz/data-digest-2025s-top-earning-genres-appsflyer-for-sale-block-blast-hits-70m-dau-app-store-earnings-more/); [Yahoo Finance / Hungry Studio PR](https://finance.yahoo.com/news/hungry-studio-block-blast-reinforces-100000899.html)
- Estimated ad revenue is about **$584k/day, or about $17.5M/month**. Lifetime IAP is only about $66k, with under $10k in 2025. — [Udonis Block Blast stats](https://www.blog.udonis.co/statistics/block-blast); [Game Industry Library](https://gameindustrylibrary.com/documents/block-blast)
- Other reports put it at "$1M a day", and it hit a peak of about $1.8M in ad revenue on Black Friday 2025. — [Gamigion](https://www.gamigion.com/block-blast-by-hungry-studio-is-doing-1m-a-day/); [Felix Braberg, 40M DAU & $1M/day](https://felixbraberg.substack.com/p/block-blast-review-what-is-behind-b38); [Felix Braberg, Black Friday 2025](https://felixbraberg.substack.com/p/the-biggest-ad-monetized-game-on)
- Tencent invested in Hungry Studio. — [36Kr](https://eu.36kr.com/en/p/3706617203732616)
- One search extract claimed "$8 ARPDAU". **This is implausible**: $584k–1M per day divided by 40–70M DAU is about $0.008–0.025 ARPDAU. Treat the $8 figure as an error.

**Woodoku (Tripledot)**
- Woodoku has about 130M lifetime downloads, about 420k in the last 30 days, and about 7.8M MAU. It makes about $500k+/month, split 26% IAP / 74% ads, and integrates 28 ad networks and 3 mediation SDKs. These are AppGoblin estimates. — [AppGoblin](https://appgoblin.info/apps/com.tripledot.woodoku)

**Royal Match (Dream Games)**
- Royal Match grossed over **$1.4B in IAP in 2025**, making it the #1 puzzle title. Candy Crush Saga grossed over **$1.1B** (Sensor Tower). — [Sensor Tower via GameDevReports](https://gamedevreports.substack.com/p/sensor-tower-us-mobile-puzzle-revenue); [Sensor Tower US puzzle](https://sensortower.com/blog/us-mobile-puzzle-4-point-6-billion-revenue)
- Players have spent over $6B lifetime in Royal Match. Dream Games' total user spending is $7B+. September 2025 IAP was about $107M. Royal Kingdom passed $300M in its first year, beating Royal Match's first year. — [App2top](https://app2top.com/news/players-have-spent-over-6-billion-in-royal-match-280790.html); [Gamigion](https://www.gamigion.com/dream-games-reaches-a-new-high-of-7b-in-user-spending/); [PocketGamer.biz](https://www.pocketgamer.biz/royal-kingdom-surpasses-300m-in-first-year-beating-royal-match/)

**Candy Crush Saga (King)**
- Figures conflict:
  - Over $1.1B IAP in 2025 (Sensor Tower, above).
  - About $75–90M/month, passing $1B for the first time, up from $980M in 2024. — [TechSpot](https://www.techspot.com/news/113475-candy-crush-generates-nearly-1-billion-annually-14.html)
  - "$876.5M in FY2025". — [Business of Apps](https://www.businessofapps.com/data/candy-crush-statistics/)
  - April 2025 was its second-highest-grossing month on record, per AppMagic. — [WN Hub](https://wnhub.io/news/analytics/item-47897)

**Market context**
- The mobile puzzle genre made over $10B in IAP in 2025 (+14% YoY), the #2 genre after strategy, with 9.7B downloads. US mobile puzzle spending was $4.6B (+30% YoY). — [Sensor Tower](https://sensortower.com/blog/us-mobile-puzzle-4-point-6-billion-revenue); [GameDevReports](https://gamedevreports.substack.com/p/sensor-tower-us-mobile-puzzle-revenue)

**Solo / small developers**
- Balatro is solo-developed (LocalThunk) but is a premium PC-to-mobile port, not a casual puzzle. It made **$21.3M in mobile revenue from 3.1M downloads** (2025). — [daily.dev summary of premium mobile report](https://daily.dev/posts/premium-mobile-games-are-back-with-releases-up-77-in-2025-mo3xb5ehx)
- Ant Smasher (Best Cool & Fun Games) was an older small-developer story (pre-2015). It was on track for about $2M/yr, about 80% from ads, with ad revenue reinvested in AdMob UA. — [Felix Braberg / search extract](https://felixbraberg.substack.com/p/the-mobile-ad-monetization-newsletter-57a) **(old; flag)**
- An older (pre-2020) "First week revenue data from an endless puzzle game on iOS" postmortem exists on Game Developer. — [Game Developer](https://www.gamedeveloper.com/business/first-week-revenue-data-from-an-endless-puzzle-game-on-ios)

### Inferences
- Block Blast's implied ARPDAU is about $0.01–0.02, which is very low. Its revenue comes from massive organic scale and retention, not from monetization depth. A solo developer copying the format would need millions of DAU to earn meaningful money: 100k DAU × $0.015 ≈ $1.5k/day at best.
- Woodoku at about $500k/month and 7.8M MAU works out to roughly $0.064 per MAU per month, which fits an ad-first block puzzle with light IAP.

### Gaps
- No verifiable 2024-26 solo-developer casual/puzzle postmortem with revenue numbers was found. Reddit and Medium were not reachable through search results.
- Hungry Studio's team size and total downloads are unconfirmed.

## 4. Platform fees and ad mediation

### Takeaway
Small developers pay a 15% store commission on both stores for their first $1M. Ad mediation is effectively a three-player market, with AppLovin MAX dominant.

### Cited Findings
- **Apple Small Business Program** gives 15% to developers with under $1M in proceeds in the previous calendar year, and to new developers. It covers paid apps, IAP and subscriptions. If you cross $1M in a year, you pay 30% for the rest of that year. Enrollment is required. — [RevenueCat](https://www.revenuecat.com/blog/engineering/small-business-program); [Appbot](https://appbot.co/blog/app-developers-apple-google-small-business-programs/)
- **Google Play** charges 15% automatically on each developer's first $1M/year, in real time, then 30% above that. Auto-renewing subscriptions are 15% from day one. — [RevenueCat](https://www.revenuecat.com/blog/engineering/small-business-program); [SplitMetrics](https://splitmetrics.com/blog/google-play-apple-app-store-fees/)
- **Mediation market (2025)**: MAX has more than half the market. MAX, LevelPlay and AdMob together hold over 90%. Among top-downloaded games, MAX is used by 73.2%, AdMob 11.4%, LevelPlay 5.7%, in-house 4.6% and FairBid 3.4%. Among top-grossing games, MAX holds about 55%. — [PocketGamer.biz: Nine facts about mediation 2025](https://www.pocketgamer.biz/nine-facts-about-the-mediation-space-in-2025/); [GameBiz Consulting](https://www.gamebizconsulting.com/newsletter/newsletter-may25); [Gamesforum](https://www.globalgamesforum.com/news/max-vs-levelplay-9-facts-about-the-mediation-space-in-2025)
- AdMob historically lagged on metrics and network coverage but is closing the gap. Unity's UA is weak compared with AppLovin's, eroding LevelPlay's share. — [Gamesforum](https://www.globalgamesforum.com/news/max-vs-levelplay-9-facts-about-the-mediation-space-in-2025)

### Inferences
- Ad revenue is not subject to store commissions. For an ads-first puzzle game, the 15% only applies to remove-ads and booster IAP. This is a structural advantage of IAA for small developers.
- Solo developers typically start on AdMob because it is simplest, then move to MAX once volume justifies the setup.

### Gaps
- No 2024-26 data on how much net ad revenue a small publisher gains from MAX versus AdMob.

## 5. Premium paid games on mobile; Apple Arcade and Netflix Games

### Takeaway
Premium is a small niche (about 4% of downloads) but was reviving in 2025, with releases up 77%. It works mostly for known PC/console brands, as with Balatro. Subscription platforms like Apple Arcade and Netflix are funded-deal alternatives, but they do not suit simple casual puzzle games unless they are distinctive.

### Cited Findings
- Premium mobile releases rose 77% in 2025, to nearly 750 titles. F2P still takes 96% of downloads. PC-to-mobile ports grew from 7 in 2024 to 23 in 2025, and port revenue went from about $7M in 2022 to about $15M in 2025. Balatro made $21.3M on mobile. — [daily.dev summary](https://daily.dev/posts/premium-mobile-games-are-back-with-releases-up-77-in-2025-mo3xb5ehx); [Prism News](https://www.prismnews.com/hobbies/mobile-gaming/apple-and-netflix-drive-surge-in-premium-mobile-game-ports)
- Apple Arcade costs $6.99/month. Netflix includes 80+ ad-free, IAP-free iPhone/iPad games in the subscription (September 2026 catalog). — [Tech Insider](https://tech-insider.org/apple-arcade-vs-google-play-pass-vs-netflix-games-2026/); [9to5Mac](https://9to5mac.com/2026/09/06/youre-paying-for-80-iphone-and-ipad-games-through-netflix-heres-the-full-catalog/)
- Industry commentary credits Arcade and Netflix with normalizing premium on phones. — [Prism News](https://www.prismnews.com/hobbies/mobile-gaming/apple-and-netflix-drive-surge-in-premium-mobile-game-ports)

### Inferences
- The "~$15M total port revenue in 2025" figure conflicts with Balatro's $21.3M alone. The port figure likely covers a narrower or different set, so both need checking before use.
- For a simple block or match puzzle, premium pricing is unlikely to compete with free clones. Free with ads plus a remove-ads IAP is the default choice.

### Gaps
- No public data on Apple Arcade or Netflix deal sizes for small developers, or on how to pitch to them.
- Google Play Pass economics were not found.
