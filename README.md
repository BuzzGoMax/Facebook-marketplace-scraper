[Facebook Marketplace Scraper](https://apify.com/sovereigntaylor/facebook-marketplace-scraper?fpr=data)

# Facebook Marketplace Scraper

Extract listings from Facebook Marketplace across all major categories. Scrape vehicles, property, electronics, clothing, furniture, and more with full detail extraction including prices, descriptions, seller information, images, conditions, and locations.

## Features

- **6 categories** -- vehicles, property, electronics, clothing, furniture, or browse all
- **Multi-term search** -- search for multiple keywords in a single run
- **Location targeting** -- 30+ pre-mapped US cities plus custom location IDs
- **Price filtering** -- set min/max price ranges
- **Radius control** -- search within a specific mile radius of your location
- **Sort options** -- best match, price low/high, or newest first
- **3 extraction strategies** for maximum data coverage:

- **Strategy 1**: HTML card parsing from browse/search pages
- **Strategy 2**: Individual listing detail page extraction
- **Strategy 3**: GraphQL/JSON relay data extraction from embedded page data
- **Anti-blocking measures** -- user agent rotation, request delays, proxy support
- **Login wall detection** -- auto-switches to mbasic.facebook.com fallback
- **CAPTCHA detection** -- detects and reports blocks gracefully
- **Deduplication** -- never scrapes the same listing twice
- **Pay-per-event billing** -- only charged for each listing successfully scraped

## Important Notes

Facebook Marketplace aggressively restricts automated access. For best results:

1. **Residential proxies are strongly recommended** -- Facebook blocks most datacenter IPs
2. **Many Marketplace features require authentication** -- public access is limited
3. **Rate limits apply** -- the scraper uses conservative delays (2-5s between requests)
4. **Results may vary by location** -- some markets have more public listings than others

## Use Cases

### Used Car Shopping

Search for vehicles across multiple cities, compare prices, and find deals on specific makes and models.

### Apartment Hunting

Monitor rental listings in your target area with price and radius filters to catch new postings quickly.

### Competitive Price Analysis

Track pricing for electronics, furniture, or other goods across different markets to understand regional pricing.

### Reseller Sourcing

Find underpriced items in your area for resale by scanning specific categories with price filters.

### Market Research

Analyze listing volumes, price distributions, and category trends across geographic areas.

### Lead Generation

Identify sellers of specific product categories for B2B outreach or partnership opportunities.

## Input

| Field | Type | Default | Description |
| --- | --- | --- | --- |
| `searchTerms` | String[] | `[]` | Keywords to search for (each term runs a separate search) |
| `location` | String | `newyork` | City name or Facebook location ID |
| `maxPrice` | Integer | `0` | Maximum price in USD (0 = no limit) |
| `minPrice` | Integer | `0` | Minimum price in USD (0 = no limit) |
| `category` | String | `all` | Category filter: `vehicles`, `property`, `electronics`, `clothing`, `furniture`, `all` |
| `radius` | Integer | `40` | Search radius in miles (0 = default) |
| `maxResults` | Integer | `500` | Maximum listings to scrape |
| `sortBy` | String | `best_match` | Sort order: `best_match`, `price_low`, `price_high`, `date_newest` |
| `proxy` | Object | *(none)* | Apify proxy configuration (residential recommended) |

### Supported Locations

| City | Code | City | Code |
| --- | --- | --- | --- |
| New York | `newyork` | San Francisco | `sanfrancisco` |
| Los Angeles | `losangeles` | Chicago | `chicago` |
| Houston | `houston` | Phoenix | `phoenix` |
| Philadelphia | `philadelphia` | San Antonio | `sanantonio` |
| San Diego | `sandiego` | Dallas | `dallas` |
| Austin | `austin` | Seattle | `seattle` |
| Denver | `denver` | Boston | `boston` |
| Nashville | `nashville` | Miami | `miami` |
| Portland | `portland` | Atlanta | `atlanta` |
| Minneapolis | `minneapolis` | Detroit | `detroit` |
| Las Vegas | `lasvegas` | Baltimore | `baltimore` |
| Milwaukee | `milwaukee` | Sacramento | `sacramento` |

You can also use Facebook's numeric location IDs for precise targeting of any area worldwide.

## Input Examples

### Used iPhones in New York under $500

```
{
    "searchTerms": ["iphone 15", "iphone 14 pro"],
    "location": "newyork",
    "category": "electronics",
    "maxPrice": 500,
    "maxResults": 200,
    "sortBy": "price_low"
}
```

### Furniture in Chicago within 20 miles

```
{
    "searchTerms": ["couch", "dining table", "bookshelf"],
    "location": "chicago",
    "category": "furniture",
    "radius": 20,
    "maxResults": 300
}
```

### Cars under $15,000 in Los Angeles

```
{
    "searchTerms": ["honda civic", "toyota camry"],
    "location": "losangeles",
    "category": "vehicles",
    "maxPrice": 15000,
    "maxResults": 500,
    "sortBy": "date_newest"
}
```

### Browse all listings in Austin

```
{
    "location": "austin",
    "category": "all",
    "maxResults": 1000
}
```

### Rental apartments in Miami, $1000-$2500

```
{
    "searchTerms": ["apartment", "1 bedroom"],
    "location": "miami",
    "category": "property",
    "minPrice": 1000,
    "maxPrice": 2500,
    "radius": 15,
    "maxResults": 200
}
```

## Output

Each listing is saved to the default dataset with the following fields:

```
{
    "title": "iPhone 15 Pro Max 256GB - Excellent Condition",
    "price": 899,
    "location": "Brooklyn, NY",
    "description": "Selling my iPhone 15 Pro Max 256GB in Natural Titanium. Phone is in excellent condition, always kept in a case with screen protector. Battery health at 97%. Comes with original box, charger, and unused EarPods. No scratches or dents.",
    "sellerName": "John D.",
    "sellerRating": 4.8,
    "images": [
        "https://scontent.xx.fbcdn.net/v/t45.1600-4/image1.jpg",
        "https://scontent.xx.fbcdn.net/v/t45.1600-4/image2.jpg",
        "https://scontent.xx.fbcdn.net/v/t45.1600-4/image3.jpg"
    ],
    "condition": "Used - Like New",
    "category": "Electronics",
    "listedAt": "2026-02-28T14:30:00.000Z",
    "url": "https://www.facebook.com/marketplace/item/1234567890123/",
    "listingId": "1234567890123",
    "attributes": null,
    "scrapedAt": "2026-03-01T10:00:00.000Z"
}
```

### Vehicle listing example:

```
{
    "title": "2021 Honda Civic EX - Low Miles",
    "price": 22500,
    "location": "Queens, NY",
    "description": "2021 Honda Civic EX with only 18,000 miles. Single owner, clean title, no accidents. Features include sunroof, Apple CarPlay, lane departure warning, and adaptive cruise control.",
    "sellerName": "AutoMax Dealers",
    "sellerRating": 4.5,
    "images": [
        "https://scontent.xx.fbcdn.net/v/t45.1600-4/car1.jpg",
        "https://scontent.xx.fbcdn.net/v/t45.1600-4/car2.jpg"
    ],
    "condition": "Used - Like New",
    "category": "Vehicles",
    "listedAt": "2026-02-27T09:15:00.000Z",
    "url": "https://www.facebook.com/marketplace/item/9876543210123/",
    "listingId": "9876543210123",
    "attributes": {
        "year": "2021",
        "make": "Honda",
        "model": "Civic EX",
        "mileage": "18,000",
        "transmission": "Automatic",
        "fuelType": "Gasoline",
        "exteriorColor": "Silver"
    },
    "scrapedAt": "2026-03-01T10:05:00.000Z"
}
```

### Minimal listing (card-only data, no detail page):

```
{
    "title": "Vintage Wooden Bookshelf",
    "price": 75,
    "location": "Manhattan, NY",
    "description": null,
    "sellerName": null,
    "sellerRating": null,
    "images": ["https://scontent.xx.fbcdn.net/v/t45.1600-4/shelf.jpg"],
    "condition": null,
    "category": "Furniture / Home",
    "listedAt": null,
    "url": "https://www.facebook.com/marketplace/item/5555555555555/",
    "listingId": "5555555555555",
    "attributes": null,
    "scrapedAt": "2026-03-01T10:10:00.000Z"
}
```

## How It Works

The scraper uses three complementary strategies to maximize data extraction:

### Strategy 1: HTML Card Parsing

Parses the server-rendered HTML of Marketplace browse and search pages. Extracts listing cards containing title, price, location, thumbnail image, and listing URL. Works on both [www.facebook.com](http://www.facebook.com) and mbasic.facebook.com.

### Strategy 2: Detail Page Extraction

Visits individual listing pages to extract the full data: complete description, all images (high resolution), seller name and rating, item condition, location details, and category-specific attributes (vehicle specs, property details).

### Strategy 3: GraphQL Relay Data

Facebook embeds pre-loaded data in script tags as serialized JSON (GraphQL relay format). This often contains structured listing data including fields not visible in the HTML. The scraper extracts and parses these payloads for additional data.

### mbasic Fallback

When the main Facebook site shows a login wall, the scraper falls back to mbasic.facebook.com, which has a simpler HTML structure that is often more accessible without authentication.

## Anti-Blocking Measures

Facebook is one of the most aggressive websites at detecting and blocking scrapers. This actor includes:

- **User agent rotation** -- 16 realistic desktop and mobile user agents
- **Referrer spoofing** -- realistic referrer headers
- **Request delays** -- 2-5 second random delays between requests
- **Rate limiting** -- max 15 requests per minute
- **Block detection** -- identifies login walls, CAPTCHAs, rate limits, and error pages
- **Strategy switching** -- automatically tries mbasic.facebook.com on login walls
- **Proxy support** -- full integration with Apify's proxy infrastructure

Despite these measures, **residential proxies are strongly recommended** for any serious Facebook scraping. Datacenter IPs are almost always blocked.

## Performance Tips

1. **Always use residential proxies** -- this is the single most important factor for success
2. **Start small** -- test with `maxResults: 10` before scaling up
3. **Use specific search terms** -- more targeted searches yield better results than broad browsing
4. **Set price filters** -- reduces the number of pages to scrape
5. **Try different locations** -- some areas have more publicly accessible listings
6. **Use the `date_newest` sort** -- freshest listings are often more accessible

## Limitations

- Facebook Marketplace increasingly requires login for full access
- Some listing details may not be available without authentication
- Image URLs may expire after a period of time
- Very high-volume scraping will trigger rate limits regardless of proxy quality
- Vehicle VIN data is only available on detail pages and not all listings include it
- Seller rating data depends on the seller having enough reviews

## Pricing (Pay Per Event)

This actor uses Apify's pay-per-event model. You are charged $0.005 for each listing successfully scraped and saved to the dataset. You are NOT charged for failed requests, blocked pages, or duplicate listings.

## Legal Notice

This actor is provided as a technical tool for research and analysis purposes. Users are responsible for ensuring their use complies with Facebook's Terms of Service and all applicable laws and regulations. The actor accesses only publicly available pages and does not circumvent any authentication mechanisms.

## Integration — Python

```
from apify_client import ApifyClient

client = ApifyClient("YOUR_API_TOKEN")
run = client.actor("sovereigntaylor/facebook-marketplace-scraper").call(run_input={
    "searchTerm": "facebook marketplace",
    "maxResults": 50
})

for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(f"{item.get('title', item.get('name', 'N/A'))}")
```

## Integration — JavaScript

```
import { ApifyClient } from 'apify-client';
const client = new ApifyClient({ token: 'YOUR_API_TOKEN' });

const run = await client.actor('sovereigntaylor/facebook-marketplace-scraper').call({
    searchTerm: 'facebook marketplace',
    maxResults: 50
});

const { items } = await client.dataset(run.defaultDatasetId).listItems();
items.forEach(item => console.log(item.title || item.name || 'N/A'));
```