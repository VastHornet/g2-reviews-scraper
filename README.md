[G2 Reviews Scraper](https://apify.com/zen-studio/g2-reviews-scraper?fpr=data)

# G2 Reviews Scraper | Real-Time Review Data Extraction (2026)

**The only G2.com scraper on Apify that returns real-time data and actually works.**

> **Apr 1, 2026** — Large-scale scrapes (5k-10k+ reviews)  ·  **Mar 10, 2026** — Seller page support

| Review Scraper Suite   •  Real user reviews from 5 platforms |
| --- |
| ![](https://images.apifyusercontent.com/CpbJedMffW_o0490Ht5EqZH2ajT5j1zOnXuS6bcScPk/w:1800/cb:1/aHR0cHM6Ly9hcGlmeS1pbWFnZS11cGxvYWRzLXByb2QuczMudXMtZWFzdC0xLmFtYXpvbmF3cy5jb20vTldZc09HOTZmTUR5OHljZGYtYWN0b3ItWFFBa29Ec3NKeVdabXlSMFctYUJpOXdvRm03ZS1nMi1zY3JhcGVyLWxvZ28ucG5n.webp)  [G2 Scraper](https://apify.com/zen-studio/g2-reviews-scraper)  ➤ You are here | ![](https://images.apifyusercontent.com/uSSGkkmBo8efRNKQtwf4u-5h7e1fkyEMGV7-_olyfYs/w:1800/cb:1/aHR0cHM6Ly9hcGlmeS1pbWFnZS11cGxvYWRzLXByb2QuczMudXMtZWFzdC0xLmFtYXpvbmF3cy5jb20vTldZc09HOTZmTUR5OHljZGYtYWN0b3IteDV3YmNoQmREZXdsMjBzM2stRDgyR2l5YlhVZC1jYXB0ZXJyYS1yZXZpZXctc2NyYXBlci1sb2dvLnBuZw.webp)  [Capterra](https://apify.com/zen-studio/capterra-reviews-scraper)  Verified reviews | ![](https://images.apifyusercontent.com/9dzA8-GKgyPEDMVl61FUs9kRIbu-J8OW4uPGrAnc7WI/w:1800/cb:1/aHR0cHM6Ly9hcGlmeS1pbWFnZS11cGxvYWRzLXByb2QuczMudXMtZWFzdC0xLmFtYXpvbmF3cy5jb20vTldZc09HOTZmTUR5OHljZGYtYWN0b3ItV0xYaG9lbm1jNXZ2NzRrUnEtVUFsM0hBakNqWi10cnVzdHJhZGl1cy1yZXZpZXctc2NyYXBlci1sb2dvLnBuZw.webp)  [TrustRadius](https://apify.com/zen-studio/trustradius-review-scraper)  ROI & feature scores | ![](https://images.apifyusercontent.com/qnPBcXc5NpI82VMqZcTXjNuaLCQEyHUkNxfH2Mc1l_8/w:1800/cb:1/aHR0cHM6Ly9hcGlmeS1pbWFnZS11cGxvYWRzLXByb2QuczMudXMtZWFzdC0xLmFtYXpvbmF3cy5jb20vTldZc09HOTZmTUR5OHljZGYtYWN0b3ItbVFWZW1rb3VJZXFoYmREWGktNUc0Y2w3NmpISi1zb2Z0d2FyZWFkdmljZS1zY3JhcGVyLWxvZ28ucG5n.webp)  [SoftwareAdvice](https://apify.com/zen-studio/softwareadvice-review-scraper)  Reviewer insights | ![](https://images.apifyusercontent.com/AaPetViSAj3hTFcbAt5w6XDmDX4_gXMKR1ptt42rJ1k/w:1800/cb:1/aHR0cHM6Ly9hcGlmeS1pbWFnZS11cGxvYWRzLXByb2QuczMudXMtZWFzdC0xLmFtYXpvbmF3cy5jb20vTldZc09HOTZmTUR5OHljZGYtYWN0b3ItclBHSGhXOXVkc2lJa00xWHctaVdxVE9lVU9HQi1yZWRkaXQtdG8tbGxtLWxvZ28ucG5n.webp)  [Reddit](https://apify.com/zen-studio/reddit-software-reviews-scraper)  Real user opinions |

### Copy to your AI assistant

Copy this block into ChatGPT, Claude, Cursor, or any LLM to start using this actor.

```
zen-studio/g2-reviews-scraper on Apify. Call: ApifyClient("TOKEN").actor("zen-studio/g2-reviews-scraper").call(run_input={...}), then client.dataset(run["defaultDatasetId"]).list_items().items for results. Key inputs: url (string, required, G2 product or seller URL), limit (integer, max reviews), sortOrder (string, most_recent/most_helpful/lowest_rated/highest_rated). Full actor spec (input schema with all params/enums/defaults, output dataset fields, README): GET https://api.apify.com/v2/acts/zen-studio~g2-reviews-scraper/builds/default (Bearer TOKEN) → inputSchema, actorDefinition.storages.dataset, readme. Get token: https://console.apify.com/account/integrations
```

## How It Works

| ![G2.com — what this Actor scrapes](https://images.apifyusercontent.com/9EeOf8HlQyWqD4FewUTeCHZTRak1gw-_CGs_ibqfphk/w:1800/cb:1/aHR0cHM6Ly9paWxpLmlvL3FRZ3RXWFYucG5n.webp) |
| --- |
| ![](https://images.apifyusercontent.com/25jfk3HJDes2UyJriJL0ds2wuIilHv7wz0bfgw5elcw/w:1800/cb:1/aHR0cHM6Ly9paWxpLmlvL3FWaFE4TjkucG5n.webp) |
| [![Step 1 — Configure your search](https://images.apifyusercontent.com/Qo-4OgjpUewVBEm7zAgOYcI9FgWsGhp4js8-Y0cOmwc/w:1800/cb:1/aHR0cHM6Ly9paWxpLmlvL3FRZUtGVlYucG5n.webp)](https://console.apify.com/actors/XQAkoDssJyWZmyR0W/input) |
| ![](https://images.apifyusercontent.com/O04Y9LHvKOvZcerfX2MpHCEmoR0uvSrI4gTqUO4x31c/w:1800/cb:1/aHR0cHM6Ly9paWxpLmlvL3FWaFF2QTcucG5n.webp) |
| [![Step 2 — Paste as input JSON or run via API](https://images.apifyusercontent.com/fjoqsMSg0MT7tYD3fqLy4NhZ_Eu9pkQQ45IoGe5-smU/w:1800/cb:1/aHR0cHM6Ly9paWxpLmlvL3FRZUt4UmEucG5n.webp)](https://console.apify.com/actors/XQAkoDssJyWZmyR0W/input) |
| ![](https://images.apifyusercontent.com/25jfk3HJDes2UyJriJL0ds2wuIilHv7wz0bfgw5elcw/w:1800/cb:1/aHR0cHM6Ly9paWxpLmlvL3FWaFE4TjkucG5n.webp) |
| ![Step 3 — Structured review data, ready for analysis](https://images.apifyusercontent.com/xXQDW64yckcksGhxHokcljrBzklry1RMJ7P5729qIhk/w:1800/cb:1/aHR0cHM6Ly9paWxpLmlvL3FRZUthVVgucG5n.webp) |

Extract reviews from any G2.com product or seller page. Sort by recency, helpfulness, or rating. Filter by star ratings. Search within review text. Get structured data ready for analysis, LLM pipelines, or export.

NEW

**Seller pages** aggregate reviews across all of a vendor's products (e.g., `https://www.g2.com/sellers/planet-dds` covers Denticon, Cloud 9, and Apteryx Imaging). Each review includes which product it belongs to.

[![Demo](https://images.apifyusercontent.com/-RDLXgQTP6MKX9OzUxGuSebw7yAX_M6IqLMKdJRD-Ok/w:1800/cb:1/aHR0cHM6Ly9hc2NpaW5lbWEub3JnL2EvSGRmc3NQVnkwWDZMU05lVy5zdmc.webp)](https://asciinema.org/a/HdfssPVy0X6LSNeW)

- **Real-time data** - Fresh reviews directly from G2.com, not cached or outdated
- **No login required** - Works without G2 account or cookies
- **LLM-ready output** - Structured JSON + markdown for n8n workflows, RAG pipelines, sentiment analysis
- **Try it free** — new Apify users get $5 in platform credits. That's ~**700 reviews** at no cost

[**Try it free**](https://console.apify.com/actors/XQAkoDssJyWZmyR0W)

## Quick Start

### Scrape Recent Reviews

```
{
  "url": "https://www.g2.com/products/notion/reviews",
  "limit": 100
}
```

### Scrape Seller Reviews (All Products Under a Vendor)

```
{
  "url": "https://www.g2.com/sellers/planet-dds",
  "limit": 100
}
```

Each review includes `productName` and `productSlug` identifying which product the review is for, plus `sellerSlug` for the vendor.

### Scrape Only Negative Reviews

Filter 1-2 star reviews to analyze competitor weaknesses or prioritize your own product fixes:

```
{
  "url": "https://www.g2.com/products/jira/reviews",
  "limit": 500,
  "sortOrder": "lowest_rated",
  "starRatings": ["1", "2"]
}
```

### Scrape All Reviews (Large Volume)

Products with thousands of reviews? Set a high limit to get everything:

```
{
  "url": "https://www.g2.com/products/hubspot-marketing-hub/reviews",
  "limit": 10000
}
```

### Search Reviews for Keywords

```
{
  "url": "https://www.g2.com/products/salesforce-salesforce-sales-cloud/reviews",
  "limit": 200,
  "searchQuery": "slow loading"
}
```

## Use Cases

### Product & Research Teams

- **Competitor analysis** - Scrape competitor's negative reviews to find gaps you can exploit
- **Prioritize fixes** - Filter your own 1-2 star reviews to see what users complain about most
- **Feature validation** - Search reviews for specific features to gauge real demand

### AI & Automation

- **RAG pipelines** - Feed reviews into vector databases for retrieval-augmented generation
- **Sentiment analysis** - Process reviews through classification models at scale
- **n8n workflows** - Automate review monitoring with scheduled runs and alerts

## Input Parameters

| Parameter | Type | Required | Default | Description |
| --- | --- | --- | --- | --- |
| `url` | string | Yes | - | G2 product or seller URL (e.g., `https://www.g2.com/products/notion/reviews` or `https://www.g2.com/sellers/planet-dds`) |
| `limit` | integer | No | 1000 | Maximum reviews to scrape (1-100,000). Values below 25 are raised to 25, so the minimum effective return is 25 (or fewer if the product has less). |
| `sortOrder` | string | No | `most_recent` | `most_recent`, `most_helpful`, `lowest_rated`, `highest_rated` |
| `starRatings` | array | No | All | Filter by ratings: `["1", "2", "3", "4", "5"]` |
| `searchQuery` | string | No | - | Text search, AND logic for multiple words (product URLs only) |
| `includeProsConsSummary` | boolean | No | `true` | Include AI-generated pros/cons summary (product URLs only) |

## Output

Each review includes: reviewer details, rating, full review text, verification status, and an LLM-ready markdown version. Product metadata is in the Pros/Cons Summary.

**Automatic URL resolution:** If a product URL has changed (G2 renames slugs periodically), the scraper automatically detects the new URL and continues scraping. When this happens, each review includes a `resolvedUrl` field with the updated URL.

```
{
  "reviewId": "11754721",
  "starRating": 3.5,
  "date": "2026-01-06",
  "reviewerName": "Nyesha D.",
  "reviewerTitle": "Community Assistant",
  "reviewerInfo": [
    "Small-Business (50 or fewer emp.)"
  ],
  "reviewerAvatarUrl": "https://lh3.googleusercontent.com/a/ACg8ocJh-IpDRhO45wX0BKAA-4XPEBgY2SIPmmDqR2DKBHH60Q=s96-c",
  "reviewerMonogram": "ND",
  "title": "Notion is helpful, but it's A LOT!",
  "text": "Ability to do MANY things, but it was a lot to handle. I did not get the training needed but that's probably why I did not understand it MUChH. | We used it across teams, but I mainly used it for social media calendar.",
  "validatedReviewer": true,
  "validatedMethod": "Business Email",
  "verifiedCurrentUser": true,
  "reviewSource": "Organic",
  "incentivized": true,
  "productSlug": "notion",
  "productName": "Notion",
  "markdownContent": "# Notion Review: Notion is helpful, but it's A LOT!\n\n**Rating:** 3.5/5 ★★★☆☆ | **Date:** 2026-01-06\n**Reviewer:** Nyesha D. — Community Assistant\n**Company:** Small-Business (50 or fewer emp.)\n**Status:** Verified (Business Email) | Current User | Incentivized\n\n## What I Like\nAbility to do MANY things, but it was a lot to handle. I did not get the training needed but that's probably why I did not understand it MUChH.\n\n## What I Dislike\nWe used it across teams, but I mainly used it for social media calendar.\n\n---\n_reviewId:11754721 | product:notion_"
}
```

## Pros/Cons Summary

In addition to individual reviews, the scraper extracts G2's AI-generated pros/cons summary. This includes aggregated insights with mention counts, plus full product metadata (ID, vendor, categories, rating, etc.).

Access via the **Output tab** in Apify Console, or fetch directly:

```
GET /v2/key-value-stores/{storeId}/records/pros-cons-summary
```

```
{
  "aiSummary": {
    "pros": [
      {
        "text": "Users love theease of usein Notion, enabling seamless organization and creativity in their work and life.(3710 mentions)",
        "keyword": "ease of use",
        "mentions": 3710
      },
      {
        "text": "Users love thestreamlining and customization featuresof Notion, enhancing work organization and efficiency with ease.(2161 mentions)",
        "keyword": "streamlining and customization features",
        "mentions": 2161
      },
      {
        "text": "Users value theAI featuresin Notion for simplifying tasks and enhancing creativity in their projects.(2034 mentions)",
        "keyword": "AI features",
        "mentions": 2034
      },
      {
        "text": "Users appreciate theorganizational capabilitiesof Notion, enhancing productivity and ensuring efficient task management.(1767 mentions)",
        "keyword": "organizational capabilities",
        "mentions": 1767
      },
      {
        "text": "Users appreciate theease of usein Notion, finding it incredibly helpful for writing and organization.(1642 mentions)",
        "keyword": "ease of use",
        "mentions": 1642
      },
      {
        "text": "Users value thecontextual understandingof Notion AI, enhancing efficiency in content creation and writing processes.(1368 mentions)",
        "keyword": "contextual understanding",
        "mentions": 1368
      }
    ],
    "cons": [
      {
        "text": "Users find thelearning curve steepat first, but resources help them adapt to Notion gradually.(1489 mentions)",
        "keyword": "learning curve steep",
        "mentions": 1489
      },
      {
        "text": "Users highlight themissing featuresin Notion, particularly for mobile access and workflow efficiency improvements.(817 mentions)",
        "keyword": "missing features",
        "mentions": 817
      },
      {
        "text": "Users find thelimited featuresof Notion's AI and page development restrictive compared to other applications.(727 mentions)",
        "keyword": "limited features",
        "mentions": 727
      },
      {
        "text": "Users findapp functionality lacking, struggling with translation features, table creation, and overall editing prompts in Notion.(680 mentions)",
        "keyword": "app functionality lacking",
        "mentions": 680
      },
      {
        "text": "Users findlimited customizationoptions in Notion, desiring more formatting and integration capabilities for enhanced usability.(660 mentions)",
        "keyword": "limited customization",
        "mentions": 660
      },
      {
        "text": "Users express frustration withlimited AI functionality, desiring improvements for better integration and user experience.(606 mentions)",
        "keyword": "limited AI functionality",
        "mentions": 606
      }
    ]
  },
  "topPros": [
    {
      "name": "Ease of Use",
      "summary": "Users love theease of usein Notion, enabling seamless organization and creativity in their work and life.",
      "keyword": "ease of use",
      "mentions": 3710,
      "sampleReviews": [
        {
          "reviewerName": "Asher F.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "Seamless Integrations and Updates, But Wishing for More Custom Styling in Notion",
          "snippet": "In addition to the extensive range of integrations with the tools I already rely on, I find the ease of using these integrations and building dashboar"
        },
        {
          "reviewerName": "Verified User",
          "companySize": "Enterprise (> 1000 emp.)",
          "rating": 5.0,
          "title": "Enterprise knowledge base",
          "snippet": "Its super powerful to be able to prompt notion AI with any question about my business. It will not only search my Notion instance, but also other conn"
        }
      ]
    },
    {
      "name": "Features",
      "summary": "Users love thestreamlining and customization featuresof Notion, enhancing work organization and efficiency with ease.",
      "keyword": "streamlining and customization features",
      "mentions": 2161,
      "sampleReviews": [
        {
          "reviewerName": "Linda L.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "the perfect site for university and organization",
          "snippet": "the ai!!!\r\nalso the pages system and how customizable it is. i love that I can add emojis and it has shortcuts that make it easy to use. the whole lay"
        },
        {
          "reviewerName": "Verified User",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 4.5,
          "title": "Notion + Notion AI make work easy!",
          "snippet": "I think that Notion and Notion AI create a streamlining experience for work and work organization. I also love the customization aspects of the site."
        }
      ]
    },
    {
      "name": "AI Features",
      "summary": "Users value theAI featuresin Notion for simplifying tasks and enhancing creativity in their projects.",
      "keyword": "AI features",
      "mentions": 2034,
      "sampleReviews": [
        {
          "reviewerName": "Fan Zhang .",
          "companySize": "Enterprise (> 1000 emp.)",
          "rating": 5.0,
          "title": "my daily tool.  Super productivity tool and my second brain",
          "snippet": "Easy configuration,  intuitive and integration with most of other apps im using.   The new AI function just makes it even better."
        },
        {
          "reviewerName": "matt h.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 4.0,
          "title": "Good online workspace",
          "snippet": "Easy to create clean workspaces to explore ideas and work through projects. Able to embed things into pages, AI helps with mundane tasks."
        }
      ]
    },
    {
      "name": "Organization",
      "summary": "Users appreciate theorganizational capabilitiesof Notion, enhancing productivity and ensuring efficient task management.",
      "keyword": "organizational capabilities",
      "mentions": 1767,
      "sampleReviews": [
        {
          "reviewerName": "Asher F.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "Seamless Integrations and Updates, But Wishing for More Custom Styling in Notion",
          "snippet": "In addition to the extensive range of integrations with the tools I already rely on, I find the ease of using these integrations and building dashboar"
        },
        {
          "reviewerName": "Juan Pablo S.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 4.0,
          "title": "Great for Organizing Daily Tasks and Improving Client Response",
          "snippet": "I live how our team’s got the daily tasks organized — it really helps us stay on track and respond faster to clients"
        }
      ]
    },
    {
      "name": "Useful",
      "summary": "Users appreciate theease of usein Notion, finding it incredibly helpful for writing and organization.",
      "keyword": "ease of use",
      "mentions": 1642,
      "sampleReviews": [
        {
          "reviewerName": "Alex S.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 4.0,
          "title": "Effortless Searching with Notion AI",
          "snippet": "Very organized and easy to find the information you need quickly using Notion AI"
        },
        {
          "reviewerName": "Sanghoon L.",
          "companySize": "Enterprise (> 1000 emp.)",
          "rating": 4.5,
          "title": "Excellent ai program",
          "snippet": "It is really excellent program for writing. I wrote one review paper with this great program. English is not easy for writing but notion gave me great"
        }
      ]
    },
    {
      "name": "AI Technology",
      "summary": "Users value thecontextual understandingof Notion AI, enhancing efficiency in content creation and writing processes.",
      "keyword": "contextual understanding",
      "mentions": 1368,
      "sampleReviews": [
        {
          "reviewerName": "matt h.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 4.0,
          "title": "Good online workspace",
          "snippet": "Easy to create clean workspaces to explore ideas and work through projects. Able to embed things into pages, AI helps with mundane tasks."
        },
        {
          "reviewerName": "Verified User",
          "companySize": "Mid-Market (51-1000 emp.)",
          "rating": 3.5,
          "title": "AI Feedback",
          "snippet": "Search functionality is great. I've been using AI feature more often"
        }
      ]
    }
  ],
  "topCons": [
    {
      "name": "Learning Curve",
      "summary": "Users find thelearning curve steepat first, but resources help them adapt to Notion gradually.",
      "keyword": "learning curve steep",
      "mentions": 1489,
      "sampleReviews": [
        {
          "reviewerName": "Liliana F.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "It's the best tool I've ever used to get organized",
          "snippet": "I think the only bad thing would be that it is a little difficult to use at the beginning, but you get used to it and you learn little by little. The"
        },
        {
          "reviewerName": "Steven N.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "Literally a second brain.",
          "snippet": "Small limitations in workflows. And I still havent worked out formulas properly."
        }
      ]
    },
    {
      "name": "Missing Features",
      "summary": "Users highlight themissing featuresin Notion, particularly for mobile access and workflow efficiency improvements.",
      "keyword": "missing features",
      "mentions": 817,
      "sampleReviews": [
        {
          "reviewerName": "Morgan P.",
          "companySize": "Mid-Market (51-1000 emp.)",
          "rating": 5.0,
          "title": "I have recommended notion to many people",
          "snippet": "I wish you could alphabetize the subfolders within notion for easier access. That is honestly the only negative i could say about notion. If You added"
        },
        {
          "reviewerName": "Verified User",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "Indispensable for Project Management and Effortless Meeting Notes",
          "snippet": "I would really like to be able to transcribe meetings directly from my browser, without needing to launch the desktop app."
        }
      ]
    },
    {
      "name": "Limited Features",
      "summary": "Users find thelimited featuresof Notion's AI and page development restrictive compared to other applications.",
      "keyword": "limited features",
      "mentions": 727,
      "sampleReviews": [
        {
          "reviewerName": "Verified User",
          "companySize": "Mid-Market (51-1000 emp.)",
          "rating": 4.0,
          "title": "Impressive AI Agent, But Needs More Page-Building Features",
          "snippet": "They could use more features when developing pages."
        },
        {
          "reviewerName": "Daniel F.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "Notion changed the entire workflow",
          "snippet": "The inbuilt AI functionality is a little limited as far as output when compared with other AI programs"
        }
      ]
    },
    {
      "name": "App Functionality",
      "summary": "Users findapp functionality lacking, struggling with translation features, table creation, and overall editing prompts in Notion.",
      "keyword": "app functionality lacking",
      "mentions": 680,
      "sampleReviews": [
        {
          "reviewerName": "Thomas C.",
          "companySize": "Mid-Market (51-1000 emp.)",
          "rating": 3.5,
          "title": "I'm now using it almost daily it's incredible and for an Alpha / Beta it's promising !",
          "snippet": "Looks like the formatting is not his strong point.\r\nThere is no way to create a new page with the translation \r\nNotion AI format text randomly when yo"
        },
        {
          "reviewerName": "DINESH  K.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "Notion Was Great; Notion AI Made It Perfect",
          "snippet": "Overall, it is working great; just some fine-tuning needed e.g. sometimes, it won't create a proper table if asked."
        }
      ]
    },
    {
      "name": "Limited Customization",
      "summary": "Users findlimited customizationoptions in Notion, desiring more formatting and integration capabilities for enhanced usability.",
      "keyword": "limited customization",
      "mentions": 660,
      "sampleReviews": [
        {
          "reviewerName": "Verified User",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "AI Writing Assistant",
          "snippet": "Not enough formatting options. Also, I wish there were better website integrations. I'd love to have one of my notions page be my website, if possible"
        },
        {
          "reviewerName": "Kullah A.",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 4.5,
          "title": "I had a notion and Notion scratched the itch",
          "snippet": "Notion's weakness? If there is one it might be that it can do so much. Secondly, sometimes it feels as though one can get lost in the formatting."
        }
      ]
    },
    {
      "name": "Limited AI Functionality",
      "summary": "Users express frustration withlimited AI functionality, desiring improvements for better integration and user experience.",
      "keyword": "limited AI functionality",
      "mentions": 606,
      "sampleReviews": [
        {
          "reviewerName": "Verified User",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "Positive Notion Experience",
          "snippet": "I wish we did not have to pay for Notion's AI. I love to use AI to summarize my notes when studying for exams. Similar tools like ChatGPT are free."
        },
        {
          "reviewerName": "Verified User",
          "companySize": "Small-Business (50 or fewer emp.)",
          "rating": 5.0,
          "title": "Notion AI is the best!",
          "snippet": "I would almost prefer there to be an easier way to make excel type of spreadsheets and use the AI to make them for you! Sometimes the AI will go on an"
        }
      ]
    }
  ],
  "productName": "Notion",
  "productSlug": "notion",
  "productId": "82623",
  "productUuid": "777a1bf6-40e7-4370-935e-af2d7b3a68d1",
  "vendorId": "59116",
  "vendorName": "Notion",
  "productType": "Software",
  "productCategory": "Knowledge Base",
  "productAverageRating": 4.6,
  "productImageUrl": "https://images.g2crowd.com/uploads/product/image/small_square/.../notion.png",
  "productCategories": ["AI Writing Assistant", "Project Management", "Note-Taking Software", "..."]
}
```

The summary includes:

- **AI Summary** - Top pros and cons with mention counts
- **Top Pros** - Categorized advantages with sample reviews
- **Top Cons** - Categorized disadvantages with sample reviews
- **Product Metadata** - Full product info (ID, vendor, category, rating, image, etc.)

Set `includeProsConsSummary: false` to skip this and only scrape reviews.

## Pricing

Pay per result. Only charged for successfully scraped reviews.

| Apify Plan | Price per 1,000 reviews |
| --- | --- |
| Basic | $6.49 |
| Starter (Bronze) | $5.49 |
| Scale (Silver) | $4.49 |
| Business (Gold) | $3.49 |

**Try it free** — new Apify users get $5 in platform credits. That's ~**700 reviews** at no cost.

## API Integration

### Python

```
from apify_client import ApifyClient

client = ApifyClient("your_api_token")
run = client.actor("zen-studio/g2-reviews-scraper").call(run_input={
    "url": "https://www.g2.com/products/slack/reviews",
    "limit": 500,
    "starRatings": ["1", "2"]
})

for review in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(f"{review['starRating']} stars: {review['title']}")
```

### JavaScript

```
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: 'your_api_token' });
const run = await client.actor('zen-studio/g2-reviews-scraper').call({
    url: 'https://www.g2.com/products/slack/reviews',
    limit: 500,
    starRatings: ['1', '2']
});

const { items } = await client.dataset(run.defaultDatasetId).listItems();
console.log(`Found ${items.length} reviews`);
```

## FAQ

**Q: How many reviews can I scrape?**
A: Up to 100,000 per run. You're only charged for reviews actually returned.

**Q: What if a product has fewer reviews than my limit?**
A: The scraper returns all available reviews and charges accordingly.

**Q: How does search query work?**
A: Multiple words use AND logic. "slow loading" matches reviews containing both words.

**Q: Can I filter by date range?**
A: Not directly. Use `sortOrder: "most_recent"` with a limit to get newest reviews.

**Q: I'm getting "Product not found" but the product exists on G2?**
A: G2 periodically renames product URLs. The scraper tries to resolve the new URL automatically. If it can't, check the product's current URL on G2 and update your input.

**Q: What's the markdownContent field?**
A: A pre-formatted markdown version of each review, ready for LLM ingestion or documentation.

## Disclaimer

Data is collected from publicly available sources and provided "as is" for informational purposes. Users are responsible for compliance with G2's terms and applicable regulations (GDPR, CCPA).

---

[**Start Scraping G2 Reviews**](https://console.apify.com/actors/XQAkoDssJyWZmyR0W)

*Turn G2 reviews into actionable product intelligence.*