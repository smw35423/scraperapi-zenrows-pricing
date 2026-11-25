# ScraperAPI vs ZenRows: Which Is Cheaper for Rendered Pages and Amazon Scrapes? (Credit Multipliers, Three Real Monthly Bills, and Every ScraperAPI Plan Priced)

100,000 JavaScript-rendered pages a month costs about $99 on ZenRows and $149 on ScraperAPI. Move that workload to 200,000 Amazon product pages and the numbers flip: ScraperAPI's $149 Startup plan holds it, while the same job on ZenRows lands between $279 and $549. Every one of those figures comes from the credit multipliers each vendor publishes, so you can redo the math for your own volumes before you pay anyone.

Below is what a credit actually buys on each platform, what three common workloads cost per month on both, why the published success rates contradict each other, and the billing rules that decide the invoice at the end of the month.

> **Most teams scraping retail or search results should start on ScraperAPI Hobby ($49/month, 100,000 credits, 20 concurrent threads), then move to Startup ($149/month, 1,000,000 credits) once rendering or Amazon/Walmart/eBay multipliers enter the picture.** New accounts get a 7-day trial with 5,000 credits and no card. Credits reset at renewal and do not roll over, so size the plan to your monthly volume instead of buying one tier up "just in case."
>
> 👉 [Compare every ScraperAPI plan and start the 7-day trial](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## What one credit buys on each platform

ScraperAPI prices per request type and per domain. A normal page costs 1 credit; add `render=true` and it costs 10. Amazon, Walmart and eBay carry a flat 5-credit rate, Google and Bing 25, LinkedIn 30, and sites sitting behind Cloudflare, DataDome, PerimeterX or Akamai add 10 credits when the bypass fires. ZenRows prices by request type only: 1 credit plain, 5 with JavaScript rendering, 10 for premium proxies, 25 for premium proxies plus rendering. ZenRows publishes no per-domain rate list, so what a hard retail page costs depends on which parameters you end up needing.

| Request type | ScraperAPI credits | ZenRows credits |
| --- | --- | --- |
| Plain HTML | 1 | 1 |
| JavaScript rendering | 10 | 5 |
| Premium proxy | 10 (25 with rendering) | 10 (25 with rendering) |
| Ultra premium proxy | 30 (75 with rendering) | Not offered |
| Amazon / Walmart / eBay | 5 | No per-domain rate |
| Google / Bing | 25 | No per-domain rate |
| LinkedIn | 30 | No per-domain rate |
| Cloudflare / DataDome / PerimeterX / Akamai | +10 per request | No per-domain rate |

Those multipliers stack, and that is where the headline credit counts get slippery. ScraperAPI's documentation lists 75 credits per request as the ceiling for `ultra_premium=true` combined with `render=true`, with domain rates of 5 to 30 credits applied on top of the base request and 10 more for rendering. At that ceiling, Hobby's 100,000 credits buy roughly 1,333 requests. The same 100,000 credits cover 4,000 Google searches at 25 credits each, or 20,000 Amazon pages at 5.

ZenRows tops out at 25 credits, which is the single biggest reason rendered work is cheaper there. Two tools make the meter visible before you commit: ScraperAPI's Domain Cost Estimator in the dashboard, and the `sa-credit-cost` response header that reports what each request actually cost. Run a few of your own URLs through the trial and read that header rather than trusting any table, including this one.

## Every ScraperAPI plan, priced

| Plan | Credits / concurrent threads | Monthly price | Best for | Sign up |
| --- | --- | --- | --- | --- |
| Free | 1,000 / 5 | $0 | Confirming a target is reachable at all | [Free tier, 1,000 credits](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Hobby | 100,000 / 20 | $49 | Plain HTML pilots, small Amazon jobs | [Hobby at $49/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Startup | 1,000,000 / 50 | $149 | ~100,000 rendered pages or 200,000 Amazon pages | [Startup at $149/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Business | 3,000,000 / 100 | $299 | Country-level geo-targeting; 50,000 rendered pages behind premium proxies | [Business at $299/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Scaling | 5,000,000 / 200 | $475 | First tier with pay-as-you-go overage | [Scaling at $475/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Professional | 10,500,000 / 300 | $975 | Around 1,000,000 rendered pages a month | [Professional at $975/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Advanced | 21,500,000 / 500 | $1,975 | Largest self-serve credit bucket | [Advanced at $1,975/month](https://www.scraperapi.com/pricing/?fp_ref=coupons) |
| Enterprise | 22,000,000+ / 500+ | Custom | Volumes above the self-serve ceiling | [Talk to sales about Enterprise](https://www.scraperapi.com/pricing/?fp_ref=coupons) |

Four plan-level details decide more purchases than the credit counts do:

- **Annual billing takes 10% off** every tier, applied automatically at checkout.
- **Country-level geo-targeting starts at Business ($299).** Hobby and Startup cover US and EU proxy locations only, which rules them out if you need Japanese Amazon listings or Brazilian retail prices.
- **Pay-as-you-go starts at Scaling ($475).** On Hobby, Startup and Business, running dry means requests pause until renewal or an upgrade; auto-upgrade is opt-in on Hobby through Professional.
- **Dashboard analytics history is 30 days on Hobby and Startup**, unlimited from Business up.

## Three monthly workloads, priced on both

This is where the two price lists stop looking similar. Each row uses the cheapest plan that holds the required credits.

| Monthly workload | ScraperAPI | ZenRows |
| --- | --- | --- |
| 100,000 rendered pages | 1,000,000 credits → Startup, $149 ($1.49 per 1,000 pages) | 500,000 credits → Launch, $99 ($0.99 per 1,000 pages) |
| 50,000 rendered pages behind premium proxies | 1,250,000 credits → Business, $299 | 1,250,000 credits; Growth ($199) holds 1,200,000, so you need the $279 tier |
| 200,000 Amazon product pages | 1,000,000 credits → Startup, $149 | 5,000,000 credits at 25 per page → Scale, $549; premium proxies alone → $279 |

**Rendered pages:** ZenRows wins by $50 per 100,000 pages, because it bills rendering at 5 credits and ScraperAPI at 10. On higher tiers the gap widens in relative terms ($0.55 vs $0.95 per 1,000 pages).

**Rendered pages behind premium proxies:** close to a tie. Both charge 25 credits per page, so 50,000 pages is 1,250,000 credits; ZenRows is $20 cheaper because its $279 tier fits the volume while ScraperAPI's $199-equivalent does not exist. If those pages sit behind Cloudflare or DataDome, ScraperAPI adds 10 credits each for 1,750,000 credits total, still inside the 3,000,000 that Business provides.

**Amazon product pages:** ScraperAPI is the clear winner. The flat 5-credit named-domain rate turns 200,000 pages into 1,000,000 credits on a $149 plan. ZenRows has to price the request type the site demands, so 25 credits per page pushes the same job to a $549 plan, and even premium proxies alone cost $279. If retail sites are the job, the named-domain rate is the cheapest line on either price list.

## Why the success-rate numbers don't agree

Three sources publish success rates for these two APIs and they point in different directions. None of them should settle your decision on its own.

**ZenRows' own benchmark** (published July 2026) ran 8 target URLs at 200 requests each, at 2 and 10 requests per second. Across the six protected targets it reports ZenRows at 99.7% and 99.9%, against ScraperAPI at 60.8% and 51.2%. The detail behind those totals: ScraperAPI returned 403 on all 200 LinkedIn requests at both speeds with a message about a plan upgrade, returned 403 on Footlocker asking for `ultra_premium=true` at 30 credits per request, and on Idealista at 10 req/s dropped to 7.5% (185 of 200 requests came back as 500s).

**ScraperAPI's own comparison pages** (2025) state 99.99% success for ScraperAPI against 99.93% for ZenRows, with no published test method. Treat that as a vendor claim, the same way you treat the ZenRows numbers.

**Proxyway's 2025 Web Scraping API Report**, the only third-party source here, put ZenRows at 70.39% at 2 req/s and 31.76% at 10 req/s, noting that ZenRows "suffered the most, likely due to hitting concurrency limits," and adding that the results may not represent its full capabilities.

Response times are just as split. In ZenRows' test, ScraperAPI was faster on protected pages (median 1.4 to 4.6 seconds versus 2.7 to 17.9) and slower on unprotected ones (2.1 and 1.5 seconds versus 0.7 and 0.5). Independent measurements disagree with each other too: one tester averaged 7.5 seconds for ScraperAPI, another measured 5.6 seconds for ScraperAPI against 6.7 for ZenRows.

The practical takeaway is to benchmark your own targets. Both vendors let you do that cheaply: ScraperAPI gives 7 days and 5,000 credits with no card, ZenRows gives 14 days with 1,000 basic or 40 protected requests. Forty protected requests is thin for a real conclusion, so pick the ten URLs that matter to you and watch both the success rate and the credits each one burns.

## Billing rules that decide your invoice

The multipliers set the sticker price; the billing rules set what you actually pay.

**ScraperAPI charges for 200 and 404 responses**, plus any request you cancel before the 70-second retry window closes. **ZenRows charges for successful requests only, and counts 404 and 410 as successful.** Both therefore bill you for dead links. If 15% of the URLs in your product catalogue have been delisted, your real cost runs about 15% above the page count on either platform, and your dataset fills with empty rows that look like results.

**Unused credits behave differently.** ScraperAPI credits do not roll over at all. ZenRows plan credits expire at renewal, though top-up packs roll over once.

Two habits cut the waste. Prune dead URLs before a large run, and set `max_cost` so a single unexpectedly expensive request cannot eat a chunk of the month's allowance. Both are cheaper than discovering the problem on the invoice.

👉 [Start on Hobby at $49/month and price your own URLs against the credit meter](https://www.scraperapi.com/pricing/?fp_ref=coupons)

## What ScraperAPI does beyond the per-page price

Once the monthly costs land within $100 of each other, operational details decide it. On these, ScraperAPI does more:

- **Sticky sessions last 15 minutes**, bound to the same IP and cookie jar. ZenRows rotates IPs on every call by default and offers a session ID that lasts 10 minutes. Five minutes matters in multi-step checkout and pagination flows.
- **Official SDKs cover Go, PHP, Ruby, Java, Python and Node.js.** ZenRows documents Python and Node.js only.
- **DataPipeline handles scheduling and delivery.** You upload URLs, set a schedule, and get results by webhook callback or file download. ZenRows has no native scheduler, so recurring jobs need external cron or Airflow, and no push mechanism, so you poll for results.
- **Structured data endpoints cover Amazon, Google, Walmart, eBay and Redfin**, returning JSON rather than HTML you parse yourself. ZenRows offers structured endpoints in beta, covering Amazon, Walmart, Zillow and Idealista, one URL per call, with a data model the vendor says may change.
- **Pay-as-you-go exists from the $475 tier.** ZenRows has no overage billing, so a spike means upgrading a plan.

## Where ZenRows is the better buy

Three situations, stated plainly:

**Your pages need rendering and you don't scrape named retail domains.** At 5 credits against 10, ZenRows costs about a third less per thousand rendered pages, and the gap holds at every tier.

**You need country-level geo-targeting on a small budget.** ZenRows makes it available on every plan, including its $19 entry tier. On ScraperAPI it starts at Business, $299 a month, which is a lot to pay for a Japanese proxy if that is your only reason for upgrading.

**You are spending under roughly $150 a month on plain HTML or mixed targets.** ZenRows' $19 Build plan with 45,000 credits is a lower floor than ScraperAPI's $49 Hobby, and its 14-day trial is twice as long.

## How to pick

- Amazon, Walmart, eBay, Google or Bing results → **ScraperAPI**. The flat named-domain rates beat per-request-type pricing by a wide margin at any real volume.
- Plain HTML at volume, or heavily defended sites above $150 a month → **ScraperAPI**, where the larger credit buckets and 10-credit bypass surcharge still fit inside one plan.
- More than 50,000 rendered pages a month on sites without named-domain rates → **ZenRows**, unless you also need scheduling or webhooks.
- Country-level targeting below $299 a month → **ZenRows**, or accept US/EU coverage on ScraperAPI's lower tiers.
- Recurring jobs you don't want to orchestrate yourself → **ScraperAPI**, because DataPipeline replaces the cron box you would otherwise maintain.

Two things to confirm before you enter a card number. First, run twenty of your real URLs through the trial and check the credits each one consumes; a 75-credit request turns Hobby's 100,000 credits into 1,333 requests, and no pricing table can tell you in advance which of your targets behaves that way. Second, decide whether you need country-level targeting in the next twelve months. If you do, the cheapest workable ScraperAPI tier is Business at $299, not Hobby at $49.

If retail, search results or plain HTML at volume is the job, Hobby is the right starting point: $49 a month, 100,000 credits, 20 concurrent threads, a 7-day trial with 5,000 credits and no card, and a 10% discount if you commit to annual billing.

👉 [Start with ScraperAPI Hobby at $49/month](https://www.scraperapi.com/pricing/?fp_ref=coupons)
