[G2 Reviews Scraper](https://apify.com/junipr/g2-reviews-scraper?fpr=data)

# G2 Reviews Scraper

Scrape G2.com software reviews, ratings, pricing tiers, alternatives, and competitive comparison data. Extract structured B2B software intelligence at scale — the first reliable dedicated G2 scraper on Apify Store.

## What Can It Do?

- Extract complete product profiles with overall ratings and per-category scores (ease of use, quality of support, ease of setup, and more)
- Scrape up to 500 reviews per product with full reviewer demographics (title, company, company size, industry, region)
- Extract structured pros, cons, and "what problems are you solving" sections from each review
- Capture pricing tiers including free versions, free trials, and per-plan pricing
- Get alternative products with ratings for side-by-side competitive analysis
- Extract G2 Grid badges (Leader, High Performer, Momentum Leader)
- Filter reviews by star rating, company size, and reviewer industry
- Extract competitor comparison win/loss data
- Flag incentivized reviews and low-review-count products

## What Data Can You Extract?

| Field | Description |
| --- | --- |
| Overall rating | Product average rating (0-5) |
| Total reviews | Total review count on G2 |
| Category ratings | Ease of use, quality of support, ease of setup, ease of admin, meets requirements, ease of doing business with, product direction |
| Rating distribution | Star distribution (1-5 counts) |
| Pricing tiers | All pricing plans with billing cycle |
| Features | Feature list with ratings |
| Alternatives | Competing products with ratings and URLs |
| Badges | G2 Grid awards (Leader, High Performer, etc.) |
| Comparisons | Head-to-head competitor win/loss data |
| Review pros/cons | Structured "what do you like/dislike" feedback |
| Reviewer profile | Name, title, company, company size, industry, region |
| Usage details | Duration of use, implementation time, switched-from product |
| Vendor info | Company name, website, HQ, employee count, revenue, description |

## How to Use

**Search by software name (zero-config):**

```
{
  "searchTerms": ["Salesforce CRM"]
}
```

**Direct product URL with more reviews:**

```
{
  "productUrls": ["https://www.g2.com/products/salesforce-crm/reviews"],
  "maxReviews": 100
}
```

**Category page scraping:**

```
{
  "categoryUrls": ["https://www.g2.com/categories/crm"],
  "maxProducts": 20,
  "maxReviews": 25
}
```

**Competitive intelligence (filtered by enterprise reviewers):**

```
{
  "searchTerms": ["CRM software"],
  "maxProducts": 10,
  "maxReviews": 50,
  "reviewFilter": "most_recent",
  "companySizeFilter": ["enterprise"],
  "includeAlternatives": true,
  "includePricing": true
}
```

## Input Configuration

| Parameter | Type | Default | Description |
| --- | --- | --- | --- |
| `productUrls` | string[] | `[]` | Direct G2 product URLs |
| `searchTerms` | string[] | `["Salesforce CRM"]` | Software names to search |
| `categoryUrls` | string[] | `[]` | G2 category pages |
| `maxProducts` | integer | `50` | Max products to scrape |
| `maxReviews` | integer | `25` | Max reviews per product (0 = product only) |
| `includeAlternatives` | boolean | `true` | Extract alternative products |
| `includePricing` | boolean | `true` | Extract pricing tiers |
| `includeCompanyInfo` | boolean | `true` | Extract vendor company details |
| `reviewFilter` | string | `"most_recent"` | `most_recent`, `most_helpful`, `highest_rated`, `lowest_rated` |
| `starFilter` | integer[] | `[]` | Filter: `[4, 5]` for 4+ star reviews only |
| `companySizeFilter` | string[] | `[]` | Filter: `small`, `mid_market`, `enterprise` |
| `industryFilter` | string[] | `[]` | Filter by reviewer industry |

## Output Format

```
{
  "url": "https://www.g2.com/products/salesforce-crm",
  "productId": "salesforce-crm",
  "productName": "Salesforce CRM",
  "overallRating": 4.3,
  "totalReviews": 18542,
  "vendor": {
    "name": "Salesforce",
    "website": "https://www.salesforce.com",
    "headquarters": "San Francisco, CA",
    "yearFounded": 1999,
    "employeeCount": "10,001+",
    "revenue": "$20B+"
  },
  "ratings": {
    "easeOfUse": 4.0,
    "qualityOfSupport": 4.1,
    "easeOfSetup": 3.5,
    "easeOfAdmin": 3.8,
    "meetsRequirements": 4.4,
    "easeOfDoingBusinessWith": 4.2,
    "productDirection": 4.5
  },
  "pricing": {
    "hasFreeVersion": false,
    "hasFreeTrial": true,
    "startingPrice": "$25/user/month",
    "tiers": [
      { "name": "Starter", "price": "$25/user/month", "billingCycle": "annual" }
    ]
  },
  "alternatives": [
    { "name": "HubSpot CRM", "rating": 4.4, "url": "https://www.g2.com/products/hubspot-crm" }
  ],
  "reviews": [
    {
      "author": { "name": "Sarah M.", "title": "VP of Sales", "companySize": "201-500 employees", "industry": "Computer Software" },
      "rating": 4,
      "pros": "Incredibly customizable, robust reporting...",
      "cons": "Steep learning curve, expensive for small teams...",
      "verified": true
    }
  ],
  "badges": ["Leader", "Best Relationship"],
  "scrapedAt": "2026-03-11T12:00:00.000Z"
}
```

## Pricing

**Pay-Per-Event:** $0.0065 per review scraped ($6.50 per 1,000 reviews)

Pricing includes all platform compute costs — no hidden fees.

| Scenario | Reviews | Cost |
| --- | --- | --- |
| Single product (25 reviews) | 25 | $0.16 |
| 10 products (25 reviews each) | 250 | $0.88 |
| Competitive landscape (100 products) | 2,500 | $8.75 |
| Full category analysis (500 products) | 12,500 | $43.75 |

Product-level data (ratings, pricing, alternatives) is included free with the first review event. Products with no reviews are not charged.

## Related Actors by Junipr

- [Capterra Reviews Scraper](https://apify.com/junipr/capterra-reviews-scraper) — Capterra B2B software reviews and ratings
- [Trustpilot Reviews Scraper](https://apify.com/junipr/trustpilot-reviews-scraper) — Consumer review intelligence
- [Glassdoor Jobs Scraper](https://apify.com/junipr/glassdoor-jobs-scraper) — Employee reviews and job data

## FAQ

### How much does it cost to scrape G2 reviews?

$6.50 per 1,000 reviews scraped (pay-per-event). Product-level data with no reviews costs 1 event per product ($0.0065). A typical competitive analysis of 10 products with 25 reviews each costs about $1.63.

### Can I get G2 pricing data?

Yes — set `includePricing: true` (default). Extracts all pricing tiers including free versions, free trials, and per-plan pricing with billing cycles. If pricing is not publicly listed on G2, the field returns null with `pricingAvailable: false`.

### Does it extract reviewer company information?

Yes — each review includes the reviewer's name, job title, company name, company size, industry, and region. You can filter reviews by company size (small, mid_market, enterprise) and industry to focus on relevant segments.

### Can I compare software products using this?

Yes — the scraper extracts alternatives listed on each product page with ratings and URLs. It also extracts head-to-head comparison data (win/loss counts) when available. Scrape multiple products to build a competitive matrix.

### Is scraping G2 legal?

Reviews and ratings on G2 are publicly viewable without requiring an account. G2 has not pursued legal action against scraping of public review data. We use respectful rate limiting, randomized delays, and residential proxies to minimize server impact. For official API access, G2 offers a paid API program.