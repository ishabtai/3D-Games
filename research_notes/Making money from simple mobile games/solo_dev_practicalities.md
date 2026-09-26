# Solo Dev Practicalities: Shipping a Simple Mobile Game on iOS + Android (2025-2026)

Research note, compiled 2026-09-26. Several primary pages (support.google.com, revenuecat.com, gamedeveloper.com, playgama.com) were blocked from direct fetch in this session; figures from them come from search-result excerpts and are marked as such. Items marked "[not re-verified this session]" are long-standing, well-documented facts with official URLs that I could not open here. Check them before quoting exact wording.

---

## 1. Fixed costs and platform gatekeeping

### Takeaway
The cash cost of entry is small: about $99/yr for Apple plus $25 once for Google, and $0 to $100 for an engine. The real hurdles are time and logistics:
- You need a Mac running current Xcode (Xcode 26 / iOS 26 SDK has been required since April 28, 2026).
- New Google Play personal accounts must run a 14-day closed test with 12 or more opted-in testers for each app before production access.
- Both stores require a privacy policy.
- Organization accounts need a D-U-N-S number.

### Cited Findings
- **Google Play closed testing:** personal developer accounts created after Nov 13, 2023 must run a closed test with at least 12 testers opted in continuously for 14 days. Only then can they apply for production access. — [Play Console Help (official, via search excerpt)](https://support.google.com/googleplay/android-developer/answer/14151465?hl=en)
  - The original rule (Nov 2023) required 20 testers. Google cut it to 12 in December 2024. — [Testers Community policy history](https://www.testerscommunity.com/blog/google-play-12-testers-policy); [PrimeTestLab](https://primetestlab.com/blog/google-play-changed-20-to-12-testers)
  - Accounts created before Nov 13, 2023 and **organization accounts are exempt**. The rule applies **per app**. Meeting 12/14 makes you *eligible* to apply; Google can still ask for more testing. — [OnTest explainer](https://ontest.app/blog/google-play-12-testers-14-days-requirement-explained); [Google Play Developer Community guide](https://support.google.com/googleplay/android-developer/community-guide/255621488/everything-about-the-12-testers-requirement?hl=en)
  - A cottage industry of paid "12 testers" services has appeared, which shows how hard it is for solo devs to find testers. — [testerscommunity.com](https://www.testerscommunity.com/)
- **Apple toolchain:** from April 28, 2026, apps uploaded to App Store Connect must be built with Xcode 26+ against the iOS 26 SDK. Xcode runs only on macOS, so a Mac is effectively required. Cloud Macs or CI such as Expo EAS, Codemagic or GitHub macOS runners are workarounds. — [Apple Developer News: upcoming SDK minimum requirements](https://developer.apple.com/news/?id=ueeok6yw); [Expo blog](https://expo.dev/blog/app-store-connect-minimum-sdk-26)
- **Apple Developer Program:** $99 USD/year. Organizations must provide a D-U-N-S number (free from Dun & Bradstreet, but it can take days to weeks). Individuals enroll under their legal name, and that name is shown as the seller. — [Apple Developer Program enrollment](https://developer.apple.com/programs/enroll/) [not re-verified this session]
- **Google Play:** one-time $25 registration fee. Organization accounts also need a D-U-N-S number (Google has required this for org accounts since 2023). — [Play Console Help](https://support.google.com/googleplay/android-developer/answer/6112435) [not re-verified this session]
- **Store commission:** Apple's App Store Small Business Program and Google Play's 15% tier on the first $1M/yr cut the commission from 30% to 15% for small developers. Apple requires you to apply. — [Apple Small Business Program](https://developer.apple.com/app-store/small-business-program/) [not re-verified this session]
- **Privacy policy:** both stores require a privacy policy URL. Apple also requires "App Privacy" nutrition labels. Ad SDKs such as AdMob bring GDPR consent (UMP) and Apple ATT prompt obligations. Modern Godot AdMob plugins ship with UMP consent support. — [Poing Studios Godot AdMob plugin](https://github.com/poingstudios/godot-admob-plugin); Apple/Google privacy policy rules [not re-verified this session]

### Inferences
- Rough minimum cash budget for year 1:
  - Stores: $124 ($99 + $25).
  - Engine license: $0 to $100.
  - Mac, if you don't own one: about $600+ for a used or base Mac mini, or a cloud Mac/CI.
  - Optional: a domain for hosting the privacy policy, and paid testers.
- Plan for **2 to 4 extra weeks on Android**: recruit 12 testers, run 14 days of testing, then wait for production-access review. First-time devs routinely underestimate this.
- If you'll ship several games, a registered organization (LLC plus D-U-N-S) avoids the closed-test rule and hides your personal name. The trade-off is paperwork time and money.

### Gaps
- I could not open the official Google help page directly. I have not verified whether Google changed the 12/14 rule again after mid-2026.
- The exact macOS minimum for Xcode 26 was not confirmed.

---

## 2. Tools / tech paths

### Takeaway
For a simple 2D puzzle game in 2025-26, Godot (free, MIT) and GameMaker ($99.99 one-time) are the lowest-friction engine paths. Unity is again viable: the runtime fee is dead and Unity Personal is free under $200K. It has the most mature ad/mediation ecosystem but is the heaviest option. An HTML5/JS canvas game wrapped with Capacitor works and has solid AdMob support. Its big benefit is that the same game can also ship to web portals. Its risk is Apple guideline 4.2 rejection if it looks like a website.

### Cited Findings
- **Unity**
  - The Runtime Fee was cancelled in Sept 2024 before it took effect.
  - With Unity 6 (released Oct 17, 2024), Unity Personal stays free and its revenue/funding ceiling doubled from $100K to $200K.
  - The "Made with Unity" splash screen became optional for Personal on Unity 6.
  - Unity Pro covers $200,001 to $24.99M, and Enterprise $25M+ (effective Jan 1, 2025).
  - Unity also raised Pro/Enterprise prices at the same time.
  - Sources: [Unity blog: Unity is canceling the Runtime Fee](https://unity.com/blog/unity-is-canceling-the-runtime-fee); [Unity pricing updates](https://unity.com/products/pricing-updates); [CG Channel](https://www.cgchannel.com/2024/09/unity-scraps-controversial-runtime-fee-but-raises-prices/)
- **GameMaker**
  - Free for non-commercial use.
  - A one-time $99.99 Professional license allows commercial export to Windows, macOS, Linux, iOS, Android, web and more.
  - Consoles need Enterprise at $79.99/mo or $799.99/yr.
  - No royalties. Pricing is unchanged since the Nov 2023 overhaul.
  - Sources: [GameMaker Get](https://gamemaker.io/en/get); [GameMaker FAQ Nov 2023](https://gamemaker.io/en/help/articles/november-2023-pricing-terms-change-faq); [Game World Observer](https://gameworldobserver.com/2023/11/22/gamemaker-new-pricing-free-non-commercial-use-one-time-pro-license)
- **Godot**
  - Free and MIT-licensed; exports to iOS and Android.
  - AdMob is available through community plugins:
    - **Poing Studios**: Godot 4.2+, GDScript and C#, editor mock ads, UMP consent, mediation. — [GitHub](https://github.com/poingstudios/godot-admob-plugin)
    - **godot-sdk-integrations/godot-admob**: banner, interstitial, rewarded, app open and native ads. It moved to the Godot SDK Integrations org in April 2025. — [GitHub](https://github.com/godot-sdk-integrations/godot-admob)
- **Capacitor (HTML5/JS wrapper)**
  - Runs the game inside WKWebView (iOS) or Chrome WebView (Android).
  - Official Capacitor docs include Games and Ads guides.
  - The `@capacitor-community/admob` plugin supports banner, interstitial, rewarded, rewarded-interstitial and app-open ads.
  - Phaser + Capacitor is a documented 2025 path. The canvas/WebGL performance problems that WKWebView used to have are reported to be largely gone.
  - Sources: [capacitor-community/admob](https://github.com/capacitor-community/admob); [Capacitor Games guide](https://capacitorjs.com/docs/guides/games); [Capacitor Ads guide](https://capacitorjs.com/docs/guides/ads); [Phaser + Capacitor tutorial 2025](https://generalistprogrammer.com/tutorials/deploy-phaser-game-mobile-capacitor)
- **Apple guideline 4.2 (Minimum Functionality)** is the main risk for wrapped web apps.
  - One developer's game was rejected as "not sufficiently different from a mobile browsing experience." The reviewer suggested Game Center leaderboards and achievements as a start, but "probably not enough." — [Apple Developer Forums thread](https://developer.apple.com/forums/thread/704430)
  - Practitioner guidance: reviewers test in Airplane Mode, and apps that need a network connection to show meaningful UI get flagged as web wrappers. — [Tapbound 4.2 guide](https://www.tapbound.com/blog/apple-guideline-4-2-minimum-functionality) (vendor blog, moderate reliability); [Ionic forum rejection report](https://forum.ionicframework.com/t/app-store-rejection-4-2-design-minimum-functionality-my-first-after-2-years-of-ionic/200908) (older, ~2020)

### Inferences
- **Mitigating 4.2 risk for a wrapped HTML5 game:**
  - Bundle all assets locally (no remote URL loading) so it works fully offline.
  - Add native touches: Game Center or haptics, native splash, no browser chrome or links out.
  - A self-contained canvas game is very different from a "wrapped website," and many such games are approved. Rejections cluster around apps that load a remote site.
- **Defold** (free, King-backed, small builds, good HTML5 export and an official ads extension ecosystem) and **Flutter Flame** (Dart; ads through Google's `google_mobile_ads` package) are also viable. I did not gather fresh 2025-26 sources on them this session.
- **Which path to pick:**
  - **Web-first (JS or Godot)** if you want web portals (Poki/CrazyGames) as a second revenue channel. Godot 4's web export works but has historically had larger downloads and threading/SharedArrayBuffer quirks, whereas native JS is lightest for portals.
  - **Unity** if you expect to rely on ad mediation such as LevelPlay/AppLovin MAX, because every ad network ships a Unity SDK first.

### Gaps
- No fresh sources were collected on Defold's or Flutter Flame's ad-extension status, or on Cordova's 2025-26 maintenance status.
- I found no quantitative data on 4.2 rejection rates for wrapped games.

---

## 3. Time to market and AI tools

### Takeaway
A simple puzzle/casual game is realistically **2 to 8 weeks of build time** for an experienced solo dev, with AI coding and art tools compressing the low end. On top of that, budget **3 to 6 weeks** of store logistics: Google's 14-day closed test, App Review, and privacy and consent setup. AI-assisted clones of trending mechanics have shipped in about 2 weeks.

### Cited Findings
- **Clone of Suika/"Watermelon Game" by Anul Agarwal:** built with ChatGPT for both gameplay code and 2D art in under 2 weeks. It earned about $10,000, mostly from web game portals plus organic mobile players (2023). — [Gameplay Level Up substack](https://gameplaydev.substack.com/p/my-ai-generated-watermelon-game-2); [Medium](https://medium.com/@anulagarwal12/i-built-a-game-using-chatgpt-in-2-weeks-that-made-10-000-1e766374749f)
- **A later game by the same dev**, also built with GPT-4, reportedly reached 60M+ players and $25,000+. Self-reported and unaudited. — [Gameplay Level Up substack](https://gameplaydev.substack.com/p/my-ai-generated-game-earned-25000)
- **QuickBits' first mobile app** ("Guess The Crypto") took about 1 month to build. (The results are in section 4.) — [itch.io devlog](https://quickbits.itch.io/guess-the-crypto/devlog/294463/how-much-has-our-first-mobile-app-generated-so-far) (~2021)

### Inferences
- The long tail of the timeline is not coding. It is store setup, the tester requirement, consent/ATT, screenshots/ASO and review cycles. Expect at least one rejection-and-resubmit cycle on iOS for a first submission.
- AI speeds up prototyping and asset generation. Note that Apple and Google require disclosure or policy compliance for some AI content, and generic AI art may hurt differentiation.

### Gaps
- I found no systematic survey of solo mobile game development time. The figures above are anecdotal.

---

## 4. Income reality

### Takeaway
Revenue follows a steep power law.
- **Sensor Tower:** the top 1% of publishers took about 92.5% of mobile game IAP revenue in 2025.
- **RevenueCat:** the median subscription app makes under $50/month after a year, and only about 17% of new apps reach $1K MRR within two years.
- **Anecdotes:** first ad-supported games often earn cents to tens of dollars.

The realistic expectation for a first simple mobile game is **$0 to $100 total**. A modest outcome is a few hundred dollars a year, and $1K+/month is a top-decile result.

### Cited Findings
- **Sensor Tower, 2025:** the top 1% of publishers captured 92.5% of IAP revenue and 79.8% of downloads. — via [Game Developer Reports substack](https://gamedevreports.substack.com/p/sensor-tower-1-of-top-gaming-companies) (secondary). Earlier Sensor Tower data (1H 2022, all apps): top 1% of publishers had 91% of revenue. — [Sensor Tower blog](https://sensortower.com/blog/top-one-percent-downloads-1h-2022) (older)
- **AppMagic:** mobile game revenue growth in 2025 was about +0.2% YoY, so the market is flat. Only 9 games crossed $1B; 828 passed $10M. — via [search summary citing AppMagic Mobile Market Landscape 2026](https://gameworldobserver.com/2026/01/21/in-2025-the-revenue-of-the-mobile-gaming-market-grew-but-only-slightly-analysis). Mobile game ad revenue exceeded $12B in 2025. — [Game World Observer](https://gameworldobserver.com/2026/07/06/in-2025-mobile-game-advertising-revenue-exceeded-12-billion-analytics)
- **RevenueCat State of Subscription Apps 2026** (subscription apps only; figures from search excerpts because the page could not be fetched):
  - 17.3% of newly launched apps reach $1K MRR within two years.
  - The top 5% earn about 400x more than the bottom 25% (up from 200x in 2024).
  - Median MRR growth was 5.3% YoY, versus 306%+ for the top decile.
  - In Gaming, the median time to $1K MRR among apps that reach it is 32 days, and Gaming has the highest $10K hit rate.
  - Sources: [RevenueCat SOSA 2026](https://www.revenuecat.com/state-of-subscription-apps); [Gaming cut](https://www.revenuecat.com/state-of-subscription-apps-2026-gaming); [RevenueCat benchmarks blog](https://www.revenuecat.com/blog/growth/subscription-app-trends-benchmarks-2026)
  - **Caveat:** the dataset covers apps using RevenueCat subscriptions, which is not representative of ad-funded casual games.
- **RevenueCat 2024:** median monthly revenue after 12 months was under $50. — [TechCrunch, Mar 2024](https://techcrunch.com/2024/03/12/most-subscription-mobile-apps-dont-make-money-new-report-shows/) (older)
- **QuickBits "Guess The Crypto"** (first mobile app, about 1 month of work, ~2021):
  - 21 downloads in the first month, 268 ad impressions, **$0.07 total** AdMob revenue.
  - Rewarded ads earned more than banners and interstitials combined.
  - Source: [itch.io devlog](https://quickbits.itch.io/guess-the-crypto/devlog/294463/how-much-has-our-first-mobile-app-generated-so-far)
- **Flippa listings** show real small-game incomes:
  - Hyper-casual Android games with about 550 active installs making $89 to $188/month in AdMob. — [Swipe It](https://flippa.com/10548430-swipe-it); [Avoid The Floor](https://flippa.com/10623470-avoid-the-floor)
  - A 1M+-download driving game at about $53K/yr, all AdMob and organic. — [Flippa listing](https://flippa.com/12293686)
  - A 7-year-old Android app with about $128K lifetime AdMob earnings and 1M+ downloads. — [Flippa](https://flippa.com/11375761-7-year-old-android-app-with-all-time-admob-earnings-of-1-28-300-downloaded-1-000-000-times-100-organic)
  - Seller-reported, unverified.
- **Long-tail solo success:** Joe Cassavaugh's 18-game "Clutter" hidden-object series (PC-focused) reportedly earns $200K+/yr, built over many years of catalog growth. — [PreMortem Games 2025 wrap-up](https://premortem.games/2025/12/31/wrapping-up-2025-celebrating-the-life-and-works-of-solo-developers/)

### Inferences
- **Ad math:** a casual ad-funded game needs roughly thousands of daily active users to reach $1K/month. Rewarded video is the best format for small games.
- **Organic discovery** for a new game with no marketing budget is near zero on both stores. Most first games stay at dozens to hundreds of downloads.
- **Catalog strategy** (many small games, cross-promotion) and web portals appear more reliable for small cash than betting on one app-store hit.

### Gaps
- I found no public distribution (median/percentiles) specific to ad-funded indie mobile games. Sensor Tower and AppMagic publish top-end concentration, not the long-tail median.
- I found no survey giving the % of *game* apps earning over $1K/month, and no verified 2025-26 r/gamedev or r/iOSProgramming puzzle-game postmortems with numbers. Reddit could not be searched effectively here.

---

## 5. Alternative "small cash" routes

### Takeaway
Web portals are the most accessible small-money channel for simple HTML5 games:
- **Poki:** 50/50 split, and 100% of revenue from traffic you bring yourself.
- **CrazyGames:** roughly 60% of ads and 70% of IAP according to 2026 jam terms.

Reported results for good casual games run about $200 to $2,000/month, with the very top of Poki reaching around €1M/yr. Selling small ad-funded apps on Flippa yields roughly 1 to 3.5x annual revenue, so tiny apps sell for hundreds of dollars.

### Cited Findings
- **Poki** splits revenue 50/50 on traffic from Poki or its marketing. You keep 100% of revenue from players you bring through your own links or community. — [Playgama comparison](https://playgama.com/blog/business-faqs/poki-vs-crazygames-vs-gamedistribution-revenue-share/) (competitor blog, via search excerpt); [LinkedIn post on Poki's 50/50 model](https://www.linkedin.com/posts/druhin_poki-godspeedgames-thebrief-activity-7457291134072025088-gpQY)
- **Poki scale:** 625M players, bootstrapped with no external funding. — [AccessNewswire press release](https://www.accessnewswire.com/newsroom/en/computers-technology-and-internet/poki-announces-milestone-of-625-million-players-without-raising-e-1148808)
- **CrazyGames** does not publish its split in the main developer docs. Its 2026 GameMaker web-jam terms list 60% of in-game ad revenue and 70% of IAP revenue to developers. — [Cinevva CrazyGames guide](https://app.cinevva.com/guides/publish-game-crazygames); [Playgama](https://playgama.com/blog/business-faqs/poki-vs-crazygames-vs-gamedistribution-revenue-share/)
- **Typical portal earnings:** a well-performing casual game on a major portal earns about $200 to $2,000/month, and the top of Poki's catalog reaches up to €1M/yr. — [Cinevva web game monetization guide](https://app.cinevva.com/guides/web-game-monetization) (secondary, via search excerpt). See also [IndieGameBusiness: 5 truths about web gaming](https://indiegamebusiness.com/web-gaming-for-indie-developers/)
- **Portals plus AI:** the Watermelon clone's roughly $10K came mainly from web portals. — [Gameplay Level Up](https://gameplaydev.substack.com/p/my-ai-generated-watermelon-game-2)
- **Flippa valuations:** smaller apps typically trade at about 2.5 to 3.5x revenue, premium apps up to 5x. Another cited band is 1.2 to 1.8x revenue for apps under $500K/yr. These figures conflict, and the listings are dominated by revenue-generating apps. — [Flippa mobile app valuation 2025](https://flippa.com/blog/mobile-app-valuation-key-methods-metrics-and-multiples-for-2025/)
- **Flippa micro-sales:** Buy-Now listings for tiny hyper-casual games earning $89 to $188/month. — [Swipe It](https://flippa.com/10548430-swipe-it); [Avoid The Floor](https://flippa.com/10623470-avoid-the-floor)

### Inferences
- **For a JS/HTML5 or Godot/Defold/GameMaker web-exported puzzle game, the best order is probably:**
  1. Submit to Poki and CrazyGames. Their curation is selective and they require their SDKs.
  2. Put it on itch.io for visibility and pay-what-you-want.
  3. Wrap it for the stores.
- **Alternatives:** publisher deals (hyper-casual publishers such as Voodoo, Homa or Kwalee test prototypes via CPI) and non-exclusive licensing to portals such as GameDistribution. These are further "small cash" options, but I did not collect fresh 2025-26 sources on them this session.
- **itch.io** defaults to a 10% platform cut, adjustable by the creator. This is from general knowledge and was not re-verified here, so check [itch.io docs](https://itch.io/docs/creators/faq).

### Gaps
- I could not fetch Poki's or CrazyGames' official developer pages, so the split figures are secondary.
- I found no verified 2025-26 data on hyper-casual publisher deal terms, itch.io median earnings, or GameDistribution's split.
