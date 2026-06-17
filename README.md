[Facebook Marketplace Scraper](https://apify.com/raidr-api/facebook-marketplace-scraper?fpr=data)

# 🛒 Facebook Marketplace Scraper

Search and scrape **any item** from [Facebook Marketplace](https://www.facebook.com/marketplace) by keyword. Find electronics, furniture, clothing, collectibles, and more with powerful filtering and instant Discord notifications.

## 🔍 What does Facebook Marketplace Scraper do?

Facebook Marketplace Scraper lets you **search for anything** on Facebook Marketplace and extract listing data automatically. Unlike category-specific scrapers, this tool works with any search query — just like typing into Facebook's search bar.

- **Search any keyword**: iPhones, PS5s, vintage furniture, bikes, concert tickets — anything listed on Marketplace
- **Multiple search terms**: Run several searches in one job with shared or individual filters
- **Price filtering**: Set min/max prices per search to find deals in your budget
- **Location-based**: Search any city, address, or postal code worldwide
- **Real-time alerts**: Get Discord notifications the moment new listings appear
- **Export anywhere**: JSON, CSV, Excel, HTML — or integrate via API

## 💡 Why scrape Facebook Marketplace?

Facebook Marketplace reaches **over 1 billion users monthly**, making it one of the largest peer-to-peer marketplaces in the world. Here's why businesses and individuals scrape it:

- **Resellers & flippers**: Find underpriced items to resell for profit
- **Deal hunters**: Monitor products and get alerts when prices drop
- **Market research**: Analyze pricing trends and demand for products
- **Inventory sourcing**: Find stock for your e-commerce business
- **Competitive analysis**: Track what competitors are selling and at what prices
- **Lead generation**: Identify sellers for outreach and partnerships

## 📊 What data can you scrape from Facebook Marketplace?

Every listing includes the following data:

| Data Point | Always Included | With Detailed Fetch |
| --- | --- | --- |
| 📸 **Photo** | ✅ Primary image | ✅ All photos |
| 📝 **Title** | ✅ | ✅ |
| 💰 **Price** | ✅ (current + strikethrough) | ✅ |
| 📍 **Location** | ✅ (city, state) | ✅ (+ coordinates) |
| 📅 **Listing Date** | ✅ (exact creation time) | ✅ (exact creation time) |
| 🔗 **URL** | ✅ | ✅ |
| 🏷️ **Status** | ✅ (sold/pending/live) | ✅ |
| 🔍 **Search Query** | ✅ | ✅ |
| 📦 **Description** | — | ✅ Full description |
| 👤 **Seller** | — | ✅ Name and type |
| 🚚 **Delivery** | — | ✅ Shipping options |
| 📊 **Condition** | — | ✅ Item condition |

## 🚀 How to scrape Facebook Marketplace

1. **Create a free Apify account** using your email
2. **Open [Facebook Marketplace Scraper](https://apify.com/your-username/facebook-marketplace-query-scraper)**
3. **Enter search terms** — What are you looking for? (e.g., "iPhone 14", "PS5", "mountain bike")
4. **Set your location** — City, address, or postal code
5. **Configure filters** — Price range, listing age, result limits
6. **Click Start** and wait for the data
7. **Download results** in JSON, CSV, Excel, or HTML

## ⬇️ Input examples

### Simple mode — Quick searches

Search for multiple items with shared settings:

```
{
  "searchMode": "simple",
  "searchTerms": ["iPhone 14", "iPhone 14 Pro", "iPhone 14 Pro Max"],
  "location": "New York, NY",
  "radiusKm": "40",
  "minPrice": 400,
  "maxPrice": 900,
  "daysListed": "7",
  "listingsPerSearch": 50
}
```

### Advanced mode — Individual filters per search

Perfect for resellers tracking different products at different price points:

```
{
  "searchMode": "advanced",
  "location": "Los Angeles, CA",
  "radiusKm": "65",
  "searches": [
    {
      "searchTerm": "PS5",
      "minPrice": 300,
      "maxPrice": 450,
      "daysListed": "1",
      "filterKeywords": "disc, with controllers"
    },
    {
      "searchTerm": "Nintendo Switch OLED",
      "minPrice": 200,
      "maxPrice": 300,
      "daysListed": "7",
      "filterKeywords": "with games, bundle"
    },
    {
      "searchTerm": "MacBook Pro",
      "minPrice": 800,
      "maxPrice": 1500,
      "daysListed": "1",
      "filterKeywords": "M1, M2, M3, 14 inch, 16 inch"
    }
  ]
}
```

## ⬆️ Output example

Each listing is returned with structured data:

**Standard output (fetchDetailedItems off):**

```
{
  "id": "26187731704185625",
  "listingId": "1224864905909124",
  "title": "Mountain Bike - Excellent Condition",
  "price": {
    "amount": "250.00",
    "currency": "CAD",
    "formatted": "CA$250"
  },
  "location": {
    "city": "Edmonton",
    "state": "AB"
  },
  "primaryImage": "https://scontent.facebook.com/v/...",
  "isSold": false,
  "url": "https://www.facebook.com/marketplace/item/1224864905909124/",
  "searchQuery": "mountain bike",
  "listing_date": 1771042631,
  "listing_date_ms": 1771042631000,
  "_fetchedAt": "2026-02-15T03:25:41.399Z"
}
```

**With detailed fetch enabled (fetchDetailedItems on):**

```
{
  "id": "26187731704185625",
  "listingId": "1224864905909124",
  "title": "Mountain Bike - Excellent Condition",
  "price": {
    "formatted": "CA$250"
  },
  "listing_date": 1771042631,
  "listing_date_ms": 1771042631000,
  "extraListingData": {
    "description": "Selling my mountain bike, barely used. 21-speed Shimano gears, front suspension, disc brakes...",
    "condition": "Used - Like New",
    "creation_time": 1771042582000,
    "seller": {
      "name": "Sarah M.",
      "type": "INDIVIDUAL"
    },
    "delivery_types": ["IN_PERSON"],
    "location": {
      "city": "Edmonton",
      "state": "AB",
      "latitude": 53.546,
      "longitude": -113.491
    }
  }
}
```

## 💰 How much does it cost to scrape Facebook Marketplace?

The scraper uses Apify's **pay-per-use** pricing. You only pay for compute resources consumed.

| Results | Standard | With Detailed Fetch |
| --- | --- | --- |
| 100 | ~$0.05 | ~$0.20 |
| 500 | ~$0.20 | ~$0.80 |
| 1,000 | ~$0.40 | ~$1.50 |

*Costs depend on number of searches, filters, and whether detailed fetching is enabled.*

**Free tier**: New users get $5 in monthly credits — enough for thousands of listings!

## 🔍 Fetch Detailed Item Info

Toggle **Fetch Detailed Item Info** to control the depth of data per listing:

|  | Standard (off) | Detailed Fetch (on) |
| --- | --- | --- |
| **Speed** | Fast | Slower (1 extra request per listing) |
| **Cost** | Low | Higher (additional proxy usage) |
| **Listing date** | ✅ Approximate (~1 min accuracy) | ✅ Exact creation time |
| **Description** | — | ✅ Full seller description |
| **Condition** | — | ✅ Item condition |
| **Seller info** | — | ✅ Name, type |
| **All photos** | — | ✅ Every listing photo |
| **Coordinates** | — | ✅ Latitude/longitude |
| **Delivery options** | — | ✅ Shipping, in-person |

**Recommendation**: Start with detailed fetch **off** for speed and cost savings. Enable it when you need description, seller info, or condition data.

## 📅 How listing dates work

Every listing automatically gets an approximate posting date — no extra cost, no extra requests. This means:

- **Age filtering always works** — filter by "Last 1 hour", "Last 24 hours", etc. without enabling detailed fetch
- **Discord timestamps always show** — "Listed 2 hours ago in Edmonton, AB"
- **Accuracy**: ~1 minute of the actual posting time

When **Fetch Detailed Item Info** is enabled, the scraper also gets the exact `creation_time` from Facebook and uses it for a second, more precise age filter pass.

## 💬 Discord notifications

Get instant alerts when new listings match your criteria:

1. **Create a Discord webhook**: Server Settings > Integrations > Webhooks > New Webhook
2. **Copy the webhook URL**
3. **Paste into the scraper's "Webhook URL" field**
4. **Configure options**: New items only, items per message, image display

**What you'll receive:**

- Listing photo (thumbnail or full size)
- Title and price
- **Live-updating relative time** — "Listed 2 hours ago in Brooklyn" (auto-updates in Discord)
- Direct link to the listing
- Available/Sold status indicator

## ⚡ Simple vs Advanced search modes

| Feature | Simple Mode | Advanced Mode |
| --- | --- | --- |
| Multiple search terms | Yes | Yes |
| Price filters | Shared across all searches | Individual per search |
| Days listed filter | Shared | Individual per search |
| Keyword filters | Shared | Individual per search |
| Results limit | Shared | Individual per search |
| Best for | Quick, similar searches | Resellers, complex monitoring |

**Use Simple mode** when searching for variations of the same product (iPhone 14, iPhone 14 Pro, iPhone 14 Pro Max).

**Use Advanced mode** when tracking different products with different price expectations (PS5 at $300-450, MacBook at $800-1500).

## 🔄 Deduplication — Track only new listings

The scraper remembers what it's seen before using stable Facebook listing IDs:

- **First run**: Collects all matching listings
- **Subsequent runs**: Only returns NEW listings not seen before
- **Discord notifications**: Only alerts you about fresh listings

This is perfect for:

- Daily monitoring of products
- Building alerts for price drops
- Avoiding duplicate entries in your database

To reset and see all listings again, disable "Skip Previously Seen" in the input.

## ✨ Tips for better results

1. **Be specific with search terms** — "iPhone 14 Pro 256GB" finds better matches than just "iPhone"
2. **Use filter keywords** — Narrow results to specific conditions or features
3. **Start with a smaller radius** — Expand if you need more results
4. **Use age filtering** — "Maximum Listing Age" catches bumped/boosted old listings that appear new
5. **Enable detailed fetch selectively** — Only when you need description, condition, or seller data
6. **Schedule regular runs** — Catch new listings as they appear

## 🔗 Integrations

Connect scraped data to your favorite tools:

- **Google Sheets** — Auto-export to spreadsheets
- **Zapier** — Trigger any workflow
- **Make (Integromat)** — Complex automation
- **Slack** — Team notifications
- **Airtable** — Organize and filter data
- **Webhooks** — Custom integrations
- **REST API** — Programmatic access

## 🛠️ Using the API

**Python example:**

```
from apify_client import ApifyClient

client = ApifyClient("YOUR_API_TOKEN")

run = client.actor("your-username/facebook-marketplace-query-scraper").call(
    run_input={
        "searchMode": "simple",
        "searchTerms": ["PS5", "PlayStation 5"],
        "location": "Chicago, IL",
        "maxPrice": 400,
        "listingsPerSearch": 50
    }
)

for item in client.dataset(run["defaultDatasetId"]).iterate_items():
    print(f"{item['title']} - {item['price']['formatted']}")
```

**Node.js example:**

```
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: 'YOUR_API_TOKEN' });

const run = await client.actor('your-username/facebook-marketplace-query-scraper').call({
    searchMode: 'simple',
    searchTerms: ['PS5', 'PlayStation 5'],
    location: 'Chicago, IL',
    maxPrice: 400,
    listingsPerSearch: 50
});

const { items } = await client.dataset(run.defaultDatasetId).listItems();
console.log(`Found ${items.length} listings`);
```

## ❓ FAQ

### What can I search for?

Anything listed on Facebook Marketplace! Electronics, furniture, clothing, vehicles, real estate, collectibles, sporting goods, musical instruments — if it's on Marketplace, you can scrape it.

### Why do I need residential proxies?

Facebook blocks datacenter IPs to prevent automated access. The scraper uses Apify's residential proxy network automatically — no extra configuration needed.

### Can I search multiple locations?

Each scraper run searches one location. For multiple locations, run the scraper multiple times with different locations, use Apify's Scheduler, or orchestrate via the API.

### Do I need "Fetch Detailed Item Info" for age filtering?

No. Age filtering works out of the box using approximate listing dates. Enabling detailed fetch adds a second, more precise filter pass using the exact creation time, but is not required.

### What's the difference between "Days Listed" and "Maximum Listing Age"?

- **Days Listed**: Facebook's built-in filter — affected by sellers bumping or boosting posts
- **Maximum Listing Age**: Uses the actual posting date — more accurate, works with or without detailed fetch

### How accurate is the listing date without detailed fetch?

The approximate listing date is accurate to within ~1 minute of the actual posting time. This is precise enough for age filtering and Discord timestamps.

### Is it legal to scrape Facebook Marketplace?

Scraping publicly available data is generally legal. This scraper only extracts publicly visible listings — no private data, no login required, no personal information collected. Use responsibly and comply with applicable laws.

### Why are some listings missing images?

Facebook sometimes restricts image access. The scraper uses the primary image from search results as a fallback when detailed images aren't available.

## 🔗 Related scrapers

- **[Facebook Marketplace Vehicle Scraper](https://apify.com/your-username/facebook-marketplace-vehicle-scraper)** — Specialized for cars, trucks, motorcycles with make/model/year/mileage filters

## 📞 Support

- **Issues?** Check the [Issues tab](https://apify.com/your-username/facebook-marketplace-query-scraper/issues)
- **Bugs?** Report with steps to reproduce
- **Features?** We welcome suggestions!
- **Custom needs?** Contact us for custom scraping solutions

---

*Facebook Marketplace Scraper is not affiliated with or endorsed by Facebook/Meta. Use responsibly and in accordance with Facebook's Terms of Service.*