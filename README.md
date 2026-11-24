# USAspending Federal Awards Scraper – Contracts & Grants

Export US federal contract, IDV, grant, loan and direct payment awards from USAspending.gov: recipient, UEI, amount, outlays, awarding agency, NAICS, PSC, assistance listing, dates and place of performance. Filter by keyword, agency, recipient, state, NAICS, amount and date. Official API, no key.

**[Run it on Apify →](https://apify.com/devteamdrew/usaspending-awards?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)** (pay per result, free Apify account to start)


**USAspending Awards Scraper** by Moxie: fast, reliable and polite, built on official/public data sources.

## What can it do?

- Competitor and teaming research: who wins which federal contracts, with UEI and amounts
- Sales prospecting: recently awarded primes to pitch subcontracting or services to
- Market sizing by NAICS, PSC, agency and state
- Grant research: who receives which assistance listings
- Pair with SAM.gov opportunities: see who won similar past work before you bid

## Data source

The official USAspending.gov API (`api.usaspending.gov`, `spending_by_award` search) run by the US Treasury's Bureau of the Fiscal Service. US government open data, no login, no key.

## Features

- **Pay only for results** (pay-per-event pricing, no monthly rental)
- **Incremental mode**: scheduled runs return only items you haven't received before
- **LLM-ready output**: optional compact Markdown per item for RAG / AI agents
- **Polite rate limiting** with automatic retries and backoff
- Clean, flat JSON you can export as CSV, Excel, JSON or via API


## Quick start

1. Create a free account at [apify.com](https://apify.com/devteamdrew/usaspending-awards?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards) and copy your API token.
2. `export APIFY_TOKEN=...`
3. Run one of the examples:

```bash
bash examples/run.sh          # curl
node examples/run.js          # JavaScript (apify-client)
python examples/run.py        # Python (apify-client)
```

Example input ([examples/input.json](examples/input.json)):

```json
{
  "awardCategories": [
    "contracts"
  ],
  "naicsCodes": [
    "5415"
  ],
  "dateType": "date_signed",
  "lastDays": 14,
  "minAmount": 100000,
  "maxItems": 20
}
```

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/usaspending-awards` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/usaspending-awards?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards) for current pay-per-result pricing.

## More data actors

- [Bluesky Scraper – Posts, Profiles & Search](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [UK Companies House Scraper – Companies & Directors](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [Hacker News Scraper – Stories, Comments & Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [npm Package Scraper – Downloads & Dependencies](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [SEC EDGAR Scraper – 10-K, 8-K & Form D Funding Filings](https://apify.com/devteamdrew/sec-edgar-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [arXiv Scraper – Paper Search, Abstracts & Authors](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [UK Government Tenders Scraper – Contracts Finder, Find a Tender](https://apify.com/devteamdrew/uk-public-tenders?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [UK CQC Care Homes & Providers Scraper – Ratings & Care Leads](https://apify.com/devteamdrew/uk-cqc-care-providers?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [SAM.gov Scraper – Federal Contract Opportunities, No API Key](https://apify.com/devteamdrew/sam-gov-opportunities?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [UK Operator Licence Scraper – HGV & Bus Operators (DVSA VOL)](https://apify.com/devteamdrew/uk-operator-licences?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)
- [EU Tenders Scraper – TED Public Procurement Notices](https://apify.com/devteamdrew/eu-ted-tenders?utm_source=github&utm_medium=readme&utm_campaign=usaspending-awards)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.
