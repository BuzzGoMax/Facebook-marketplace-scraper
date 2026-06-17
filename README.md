[Facebook Marketplace Scraper](https://apify.com/crowdpull/facebook-marketplace-scraper?fpr=data)

# CrowdPull FB Marketplace Scraper

Extract listings from **Facebook Marketplace** worldwide — no login or cookies required.

No browser automation — just fast, lightweight HTTP requests using Facebook's internal GraphQL API. Works with any location Facebook Marketplace supports.

## Features

- **No login required** — extracts listings anonymously from public marketplace
- **Works worldwide** — any city Facebook Marketplace supports (US, Europe, Asia, Latin America, etc.)
- **Two input modes** — paste marketplace URLs directly, or just enter a city/neighborhood/ZIP code
- **Keyword search** — filter by product name, category, or description
- **Category URLs** — paste category-specific URLs (e.g., `/marketplace/chicago/home-improvements`)
- **Price filtering** — set minimum and maximum price thresholds
- **Multi-URL support** — scrape multiple locations or categories in a single run
- **Smart Scrape (dedup)** — skip listings already scraped in previous runs
- **Date filtering** — set `untilDate` to only extract listings from a specific date onward
- **Strict filtering** — exclude broad matches and listings from outside the target location
- **Position tracking** — each listing includes its original position in the search results
- **Full listing data** — title, price, location, image, condition, delivery options
- **Rich detail mode** — enable `includeDetails` for full description, all photos, vehicle specs (make, model, odometer, colors), and listing status
- **Pagination** — automatically loads all results via Relay cursors
- **No browser** — lightweight HTTP requests only, minimal compute cost

## Smart Scrape: How It Saves You Money

Enable **Smart Scrape** to skip listings you've already extracted. The scraper maintains a persistent cache per location that survives across runs indefinitely.

|  | Without Smart Scrape | With Smart Scrape |
| --- | --- | --- |
| **Run 1** (100 listings) | 100 extracted | 100 extracted |
| **Run 2** (20 new) | 100 extracted | 20 new + 80 cache checks |
| **Run 3** (20 new) | 100 extracted | 20 new + 80 cache checks |
| **Monthly (daily runs)** | 3,000 extracted | ~700 extracted + ~2,300 cache checks |
| **Savings** | — | **~60% cheaper** |

### Refresh Window

Set `refreshWindowDays` to re-check recent listings for price changes. For example, `refreshWindowDays: 7` re-scrapes listings from the last 7 days even if cached, so you always get fresh pricing data.

## What you get per listing

| Field | Description |
| --- | --- |
| `listingId` | Unique Facebook listing ID |
| `title` | Listing title |
| `price` | Price in cents (e.g., 250000 = $2,500.00) |
| `priceFormatted` | Human-readable price (e.g., "$2,500") |
| `currency` | Currency code (USD, EUR, GBP, etc.) |
| `location` | City and state where the item is listed |
| `listingUrl` | Direct link to the listing |
| `imageUrl` | Primary listing image URL |
| `createdAt` | ISO 8601 timestamp of listing creation |
| `sellerName` | Seller's display name (when available) |
| `sellerId` | Seller's Facebook ID (when available) |
| `sellerType` | Account type (User, Page, etc.) |
| `condition` | Item condition (new, used, etc.) |
| `availability` | Listing status |
| `deliveryTypes` | Available delivery/shipping methods |
| `position` | Original position in search results feed |
| `sourceUrl` | The marketplace URL that was scraped |
| `scrapedAt` | ISO 8601 timestamp of extraction |

### Detail fields (when `includeDetails` is enabled)

| Field | Description |
| --- | --- |
| `description` | Full listing description text |
| `allPhotos` | Array of all photo URLs (not just the primary) |
| `isSold` | Whether the listing has been sold |
| `isPending` | Whether the listing is pending sale |
| `inventoryCount` | Quantity available (for multi-item listings) |
| `vehicleMake` | Vehicle make (e.g., "Chevrolet") |
| `vehicleModel` | Vehicle model (e.g., "Monte Carlo") |
| `vehicleYear` | Vehicle model year |
| `vehicleOdometerMiles` | Odometer reading in miles |
| `vehicleExteriorColor` | Exterior color |
| `vehicleInteriorColor` | Interior color |
| `vehicleFuelType` | Fuel type |
| `vehicleCondition` | Vehicle condition |
| `vehicleNumberOfOwners` | Number of previous owners |
| `vehicleSellerType` | Dealer or private seller |
| `vehicleEngineSize` | Engine displacement |
| `vehicleGasMileage` | Fuel economy (combined or city) |

## How it works

1. Parses your input — marketplace URLs are used directly; location names are resolved to Facebook Place IDs via the internal typeahead API for accurate geo-targeting
2. Fetches the marketplace page anonymously via TLS-fingerprinted HTTP
3. Extracts authentication tokens (`lsd`, `datr`) and location coordinates from the page SSR data
4. Parses search-filtered listings from page HTML (SSR) for page 1, then queries GraphQL for pagination
5. Paginates via Relay cursors until `maxListings` reached or feed exhausted
6. Optionally enriches each listing with detail page data (description, photos, vehicle specs)
7. Deduplicates against cache if Smart Scrape is enabled

## Input examples

### Paste marketplace URLs (power users)

```
{
  "marketplaceUrls": [
    "https://www.facebook.com/marketplace/chicago",
    "https://www.facebook.com/marketplace/chicago/search/?query=furniture"
  ],
  "maxListings": 100
}
```

### Enter location + search (quick start)

```
{
  "location": "São Paulo",
  "searchQuery": "furniture",
  "maxListings": 50
}
```

### With listing details (rich data)

```
{
  "marketplaceUrls": [
    "https://www.facebook.com/marketplace/chicago/vehicles"
  ],
  "maxListings": 25,
  "includeDetails": true
}
```

### Smart Scrape (incremental monitoring)

```
{
  "marketplaceUrls": [
    "https://www.facebook.com/marketplace/chicago"
  ],
  "maxListings": 100,
  "enableDedup": true,
  "refreshWindowDays": 7
}
```

## Output example

```
{
  "listingId": "1731225464511434",
  "title": "2001 Chevrolet Monte Carlo · SS Coupe 2D",
  "price": 250000,
  "priceFormatted": "$2,500",
  "currency": "USD",
  "location": "Buffalo Grove, Illinois",
  "listingUrl": "https://www.facebook.com/marketplace/item/1731225464511434/",
  "imageUrl": "https://scontent-det1-1.xx.fbcdn.net/v/...",
  "createdAt": "2026-02-25T18:00:00.000Z",
  "sellerName": "",
  "sellerId": "",
  "sellerType": "",
  "condition": null,
  "availability": null,
  "deliveryTypes": ["LOCAL_PICK_UP"],
  "description": "2001 Monte Carlo SS, runs great, clean title. 157K miles.",
  "allPhotos": ["https://scontent-det1-1.xx.fbcdn.net/v/photo1...", "https://scontent-det1-1.xx.fbcdn.net/v/photo2..."],
  "isSold": false,
  "vehicleMake": "Chevrolet",
  "vehicleModel": "Monte Carlo",
  "vehicleYear": 2001,
  "vehicleOdometerMiles": 157857,
  "vehicleExteriorColor": "red",
  "vehicleCondition": "USED",
  "sourceUrl": "https://www.facebook.com/marketplace/chicago",
  "scrapedAt": "2026-03-05T12:00:00.000Z"
}
```

Detail fields (`description`, `allPhotos`, vehicle specs, etc.) are only populated when `includeDetails` is enabled.

## Other CrowdPull Facebook scrapers

- **[Facebook Group Posts Scraper](https://apify.com/crowdpull/facebook-group-posts-scraper)** — extract posts from any public Facebook group
- **[Facebook Post Comment Scraper](https://apify.com/crowdpull/facebook-post-comment-scraper)** — extract all comments and replies from any public post with reaction breakdowns and spam signals

## Cost estimate

This Actor uses **no browser** — just lightweight HTTP requests.

| PPE Event | Description | Cost |
| --- | --- | --- |
| `actor-start` | One-time per run | $0.005 |
| `listing-extracted` | Per listing pushed to dataset | Per-1K pricing (see Store) |
| `listing-details` | Per listing enriched with detail page data | Per-1K pricing (see Store) |
| `cache-check` | Per listing skipped by Smart Scrape | Reduced rate (see Store) |

A typical run extracting 100 listings costs ~$0.01-0.03 in platform fees. With `includeDetails` enabled, add ~$0.03/100 listings for detail enrichment.

## Use cases

- **Market research** — analyze local pricing trends for specific product categories
- **International price comparison** — compare marketplace prices across cities and countries
- **Competitive intelligence** — monitor competitor inventory and pricing
- **Arbitrage** — find underpriced items across locations for resale
- **Lead generation** — extract seller data from niche product categories
- **Price monitoring** — track price changes over time with Smart Scrape
- **Real estate** — monitor furniture/appliance listings near rental properties

## Is it legal to scrape Facebook Marketplace?

This Actor extracts **publicly visible** data from Facebook Marketplace. Here are the key legal considerations:

- **Public data**: Only publicly listed items are accessible. No private or restricted content is extracted.
- **No authentication by default**: The scraper works anonymously without any Facebook account, accessing only what any visitor can see.
- **Terms of Service**: Web scraping of public data has been upheld in multiple court rulings (hiQ Labs v. LinkedIn, 2022). However, Facebook's Terms of Service restrict automated data collection. Use this tool responsibly and in compliance with applicable laws.
- **GDPR/CCPA**: Extracted data may contain seller names and profile IDs. If you process this data in the EU/EEA or for California residents, ensure you have a lawful basis under GDPR/CCPA.
- **Rate limiting**: The scraper includes built-in delays and respects Facebook's rate limits to minimize server impact.

**You are responsible for ensuring your use of this data complies with all applicable laws and regulations in your jurisdiction.**

## Limitations

- `doc_id` may rotate when Facebook redeploys — report issues if extraction stops
- Facebook rate limits apply; residential proxies recommended
- Anonymous mode may return fewer results than authenticated browsing
- Price filtering depends on Facebook's GraphQL variable support (may vary by region)
- `includeDetails` adds ~1 second per listing (detail page fetch + rate limiting)
- Seller data (name, ID) is not available in anonymous mode on detail pages
- Location resolution uses Facebook's internal typeahead API — works for any city, neighborhood, or ZIP code worldwide