[G2 Reviews Scraper](https://apify.com/focused_vanguard/g2-reviews-scraper?fpr=data)

# G2 Reviews Scraper

Scrape product reviews from **G2.com** (B2B software marketplace) and get **clean, structured review data** with real publish dates.

## Why this Actor beats most “G2 scrapers”

- **Real review schema** (no unrelated/irrelevant fields)
- **Publish date included**: `date_posted`
- **Most recent first** + optional `lookbackDays` to stop early and save cost
- **URL normalization**: if the input is missing `/reviews`, it will be fixed automatically
- **Predictable limits**: cap results with `maxReviews` (max 500) and `maxPages`

Don’t have a G2 URL? Use the companion actor **“G2 Reviews by Company Domain”** to auto-find the correct page first.

## Features

- Extract **ratings**, **pros/cons**, and full review text
- Extract reviewer metadata (when available): **job title**, **company size**, **industry**
- **Recent-first** scraping with optional early stop via `lookbackDays`
- **Automatic pagination**
- **Structured output** in Apify dataset (easy to export to JSON/CSV)

## Input

| Field | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | Yes | G2 product URL (with or without `/reviews`) |
| `maxReviews` | integer | No | Maximum reviews (default: 100, max: 500) |
| `maxPages` | integer | No | Maximum pages (default: 10) |
| `lookbackDays` | integer | No | Stop when reviews are older than N days (saves cost) |

### Example Input

```
{
    "url": "https://www.g2.com/products/postman/reviews",
    "maxReviews": 100,
    "lookbackDays": 90
}
```

## Output

Each dataset item is one review. Key fields:

| Field | Description |
| --- | --- |
| `id` | Unique review ID |
| `content` | Full review text |
| `pros` | What user likes |
| `cons` | What user dislikes |
| `author` | Reviewer name |
| `author_title` | Job title |
| `author_company_size` | Company size (when available) |
| `author_industry` | Industry (when available) |
| `date_posted` | Publish date/time |
| `review_url` | Direct link to the review (when available) |
| `product_url` | Product page URL |

## Use Cases

- **Competitive Analysis**: Monitor competitor product reviews
- **Sales Intelligence**: Understand customer pain points
- **Market Research**: Analyze software category trends
- **Product Development**: Learn what features users want

## Pricing

Recommended Apify Store pricing (Pay per result): **$4.99 / 1,000 reviews**.

Example costs:

- 100 reviews: ~$0.50
- 500 reviews: ~$2.50
- 1,000 reviews: $4.99