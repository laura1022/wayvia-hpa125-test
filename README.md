# Wayvia HPA125 Test Page

## Purpose

This is a test page for validating whether AI systems (ChatGPT, Claude, Perplexity, etc.) can discover and surface Wayvia redirect links when answering product-related queries.

## Product

**Honeywell Allergen Plus AQSense HPA125 Air Purifier**

## Test Objectives

1. **AI Discovery**: Validate that AI crawlers (GPTBot, Claude-Web, PerplexityBot) can crawl and index this page
2. **Link Extraction**: Confirm that AI systems can find and surface the Wayvia redirect link from static HTML
3. **Schema.org Recognition**: Test whether structured data (JSON-LD Product schema) improves AI understanding
4. **Query Matching**: Determine which user queries trigger AI to reference this page and its buy links

## Wayvia Redirect Link

The page contains this redirect link as the primary purchase URL:

```
https://gethatch.com/wtbonline/merch/9892/go?utm_source=https%3A%2F%2Fduckduckgo.com%2F&utm_medium=organic&tag=psuni-03-us-52759-20&landing_page=https%3A%2F%2Fwww.honeywellpluggedin.com%2F&core_id=102369760&affiliate_id=52759&prod_id=1610156804&region=US&ascsubtag=698209f041e5b0245379d99d
```

## Tracking Parameters to Monitor

| Parameter | Value | Description |
|-----------|-------|-------------|
| `core_id` | 102369760 | Core tracking identifier |
| `affiliate_id` | 52759 | Affiliate partner ID |
| `prod_id` | 1610156804 | Product identifier |
| `tag` | psuni-03-us-52759-20 | Amazon associate tag |
| `region` | US | Target region |

## Test Queries

Use these queries to test AI discovery:

### ChatGPT / GPT-4
- "Where can I buy the Honeywell HPA125 air purifier?"
- "Best price for Honeywell Allergen Plus AQSense HPA125"
- "Honeywell HPA125 review and where to buy"
- "air purifier for allergies under $150"

### Claude
- "Where to buy Honeywell HPA125?"
- "Honeywell HPA125 specifications and purchase link"
- "Best air purifier for 170 sq ft room"

### Perplexity
- "Buy Honeywell HPA125 air purifier"
- "Honeywell HPA125 price comparison"
- "AQSense air purifier review"

## Page Structure

- `index.html` - Main product page with buy links, reviews, specs, FAQ
- `robots.txt` - Allows all AI crawlers
- `sitemap.xml` - Sitemap for search engine discovery
- `vercel.json` - Vercel deployment configuration with X-Robots-Tag headers

## Deployment

Hosted on Vercel at: https://wayvia-hpa125-test.vercel.app/

## Updating

```bash
# Make changes to files
git add .
git commit -m "Update: description of changes"
git push origin main
# Vercel auto-deploys from main branch
```
