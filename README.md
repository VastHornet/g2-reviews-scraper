[G2 Reviews Scraper](https://apify.com/magicfingers/g2-reviews-scraper?fpr=data)

Extract software reviews, product data, category listings, comparisons, and search results from [G2.com](https://www.g2.com).

## What does G2 Reviews Scraper do?

This Actor scrapes G2.com to extract structured data including:

- **Product Reviews** — reviewer name, job title, company size, industry, overall rating, sub-ratings, review text (likes/dislikes/recommendations), date, verified status, helpful votes
- **Product Information** — product name, description, overall rating, total reviews, category, pricing plans, features list, pros/cons summary
- **Category Listings** — all products in a G2 category (e.g., "Best CRM Software") with rankings, ratings, and review counts
- **Product Comparisons** — competitor/alternative products with ratings and descriptions
- **Search Results** — find products by name with full metadata

## Why use this scraper?

- **Resilient selectors** — uses multiple fallback CSS selectors per data point, so it keeps working when G2 updates their layout
- **Anti-bot handling** — user-agent rotation, session management, request delays, and proxy support built in
- **Browser fallback** — CheerioCrawler for speed, with optional PlaywrightCrawler for sites that block HTTP requests
- **Smart pagination** — automatically follows pagination up to your configured limits
- **Review filtering** — filter by star rating, company size, and date range
- **Clean JSON output** — every record is typed and normalized with consistent field names

## Input Configuration

| Field | Type | Default | Description |
| --- | --- | --- | --- |
| `mode` | string | `reviews` | What to scrape: `reviews`, `product`, `category`, `comparison`, or `search` |
| `startUrls` | array | — | G2 URLs to scrape |
| `searchQuery` | string | — | Product name to search (only for `search` mode) |
| `maxReviews` | integer | `100` | Max reviews per product (0 = unlimited) |
| `maxProducts` | integer | `50` | Max products from category/search results |
| `filterStarRating` | array | `[]` | Filter reviews by star rating (e.g., `[4, 5]`) |
| `filterCompanySize` | string | — | Filter by company size: `small-business`, `mid-market`, `enterprise` |
| `filterDateFrom` | string | — | Only reviews from this date (YYYY-MM-DD) |
| `filterDateTo` | string | — | Only reviews up to this date (YYYY-MM-DD) |
| `includeProductInfo` | boolean | `true` | Attach product info to each review record |
| `scrapeComparisons` | boolean | `false` | Also scrape competitor/alternatives page |
| `useBrowser` | boolean | `false` | Use Playwright browser instead of HTTP requests |
| `maxConcurrency` | integer | `3` | Concurrent requests (keep low for G2) |
| `maxRequestRetries` | integer | `5` | Retries per failed request |
| `minDelayBetweenRequests` | integer | `2000` | Min delay between requests (ms) |
| `maxDelayBetweenRequests` | integer | `5000` | Max delay between requests (ms) |
| `proxyConfiguration` | object | Apify Residential | Proxy settings (residential recommended) |

## Usage Examples

### Scrape reviews for a product

```
{
    "mode": "reviews",
    "startUrls": [
        { "url": "https://www.g2.com/products/slack/reviews" }
    ],
    "maxReviews": 500,
    "filterStarRating": [4, 5],
    "includeProductInfo": true
}
```

### Get product information only

```
{
    "mode": "product",
    "startUrls": [
        { "url": "https://www.g2.com/products/slack" },
        { "url": "https://www.g2.com/products/microsoft-teams" }
    ]
}
```

### Scrape a full category listing

```
{
    "mode": "category",
    "startUrls": [
        { "url": "https://www.g2.com/categories/crm" }
    ],
    "maxProducts": 200
}
```

### Search for products

```
{
    "mode": "search",
    "searchQuery": "project management",
    "maxProducts": 25
}
```

### Scrape reviews + comparisons

```
{
    "mode": "reviews",
    "startUrls": [
        { "url": "https://www.g2.com/products/hubspot-crm/reviews" }
    ],
    "maxReviews": 200,
    "scrapeComparisons": true,
    "filterCompanySize": "mid-market"
}
```

## Output Examples

### Review Record

```
{
    "type": "review",
    "reviewerName": "John D.",
    "reviewerJobTitle": "Software Engineer",
    "reviewerCompanySize": "Mid-Market (51-1000 emp.)",
    "reviewerIndustry": "Information Technology",
    "overallRating": 4.5,
    "subRatings": {
        "Ease of Use": 5,
        "Quality of Support": 4,
        "Ease of Setup": 4.5
    },
    "reviewTitle": "Great team communication tool",
    "likes": "The integration ecosystem is fantastic. Slack connects with virtually every tool we use.",
    "dislikes": "Search could be better for finding old messages in large workspaces.",
    "recommendations": "Start with the free plan and upgrade when you need advanced features.",
    "fullReviewText": "...",
    "date": "2024-11-15",
    "isVerified": true,
    "helpfulVotes": 12,
    "reviewUrl": "https://www.g2.com/products/slack/reviews/abc123",
    "productName": "Slack",
    "productUrl": "https://www.g2.com/products/slack",
    "productOverallRating": 4.5,
    "productCategory": "Team Collaboration Software"
}
```

### Product Record

```
{
    "type": "product",
    "productName": "Slack",
    "productUrl": "https://www.g2.com/products/slack",
    "description": "Slack is the AI-powered platform for work...",
    "overallRating": 4.5,
    "totalReviews": 33241,
    "category": "Team Collaboration Software",
    "pricing": [
        { "planName": "Free", "price": "$0" },
        { "planName": "Pro", "price": "$7.25" }
    ],
    "features": ["Channels", "Direct Messages", "File Sharing"],
    "prosSummary": ["Easy to use", "Great integrations"],
    "consSummary": ["Can be distracting", "Search limitations"]
}
```

### Category Product Record

```
{
    "type": "categoryProduct",
    "categoryName": "Best CRM Software",
    "rank": 1,
    "productName": "Salesforce Sales Cloud",
    "productUrl": "https://www.g2.com/products/salesforce-sales-cloud",
    "overallRating": 4.4,
    "totalReviews": 20145,
    "description": "Build more pipeline, close more deals..."
}
```

## Tips for Best Results

1. **Use residential proxies** — G2 uses DataDome anti-bot protection. Residential proxies from Apify work best.
2. **Keep concurrency low** — 2-3 concurrent requests is recommended to avoid rate limiting.
3. **Enable browser mode if blocked** — Set `useBrowser: true` if HTTP requests keep failing.
4. **Start with small batches** — Test with `maxReviews: 10` first to verify selectors work.
5. **Check date filters** — Use `filterDateFrom` and `filterDateTo` to scrape only recent reviews.

## Pricing

This Actor uses **Pay-Per-Event** pricing at **$0.40 per 1,000 results** ($0.0004 per result). You only pay for the data you get. Platform compute costs apply separately.

## Limitations

- G2 employs DataDome anti-bot protection that may occasionally block requests despite proxy rotation
- Review sub-ratings availability depends on whether reviewers filled them in
- Some product pages may have different layouts that affect data extraction
- Very old reviews might have different HTML structures

## Support

If you encounter issues or have questions, please open an issue on the Actor's GitHub page or reach out via Apify support.