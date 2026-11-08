# Zoopla UK Property & Agent Directory Scraper

[![Apify Store](https://img.shields.io/badge/Apify%20Store-View%20Actor-brightgreen?logo=apify)](https://apify.com/misterkhan/zoopla-scraper)
[![GitHub stars](https://img.shields.io/github/stars/crawlomatic/zoopla-uk-scraper?style=social)](https://github.com/crawlomatic/zoopla-uk-scraper)
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python SDK](https://img.shields.io/badge/SDK-Python-3776AB?logo=python&logoColor=white)](https://github.com/apify/apify-client-python)
[![Node.js SDK](https://img.shields.io/badge/SDK-Node.js-339933?logo=node.js&logoColor=white)](https://github.com/apify/apify-client-js)

> Extract UK homes for sale and to rent, Zed-Index price estimates, and estate agent contacts from Zoopla.

---

## ⚡ Quick Start

You can run this scraper directly via the **[Apify Store Web Console](https://apify.com/misterkhan/zoopla-scraper)** with zero setup, or integrate it into your Python / Node.js backend using the code below.

### 🐍 Python Quickstart

```bash
pip install apify-client
```

```python
from apify_client import ApifyClient

# Initialize the ApifyClient with your API token
# Get your token from https://console.apify.com/account/integrations
client = ApifyClient("YOUR_APIFY_TOKEN")

# Configure input parameters
run_input = {
  "startUrls": [
    {
      "url": "https://www.zoopla.co.uk/for-sale/property/london/"
    }
  ],
  "maxItems": 25
}

print("🚀 Launching Zoopla UK Property & Agent Directory Scraper on Crawlomatic Engine...")
run = client.actor("misterkhan/zoopla-scraper").call(run_input=run_input)

# Fetch results from the Actor's default dataset
dataset_items = client.dataset(run["defaultDatasetId"]).list_items().items
print(f"✅ Successfully fetched {len(dataset_items)} records!")

for item in dataset_items[:3]:
    print(item)
```

---

### 🟢 Node.js / JavaScript Quickstart

```bash
npm install apify-client
```

```javascript
import { ApifyClient } from 'apify-client';

// Initialize the ApifyClient with your API token
const client = new ApifyClient({
    token: 'YOUR_APIFY_TOKEN',
});

// Configure input parameters
const input = {
  "startUrls": [
    {
      "url": "https://www.zoopla.co.uk/for-sale/property/london/"
    }
  ],
  "maxItems": 25
};

console.log('🚀 Launching Zoopla UK Property & Agent Directory Scraper...');
const run = await client.actor('misterkhan/zoopla-scraper').call(input);

// Fetch results
const { items } = await client.dataset(run.defaultDatasetId).listItems();
console.log(`✅ Extracted ${items.length} records!`);
console.dir(items.slice(0, 3));
```

---

# 🇬🇧 Zoopla UK Property Scraper [From 💰$0.75/1K]

**[From $0.75/1K] Extract property listings from Zoopla UK Property (zoopla.co.uk) across London, Bristol & Edinburgh — prices in GBP, bedrooms, bathrooms, floor area, addresses, coordinates, photos & agent details.**

Paste one or more **Zoopla UK Property** (`zoopla.co.uk`) search or property URLs and extract structured real estate listings across **London, Bristol & Edinburgh**. Download your dataset in **Excel, CSV, or JSON**, or connect directly via API, Google Sheets, Make, or n8n.

> 🛡️ **Zero Proxy Configuration Required:** Anti-blocking and regional routing are **handled automatically out of the box** — just paste your target URLs and click **Start**.

---
## ✨ What Makes This Different

| Feature | Why It Matters |
|---|---|
| **Built for Zoopla UK Property (`zoopla.co.uk`)** | Tuned specifically for `zoopla.co.uk` search pagination, listing cards, and structured property schemas across United Kingdom. |
| **Zero Proxy or Login Setup** | Works out of the box with country-targeted residential routing — just paste your `zoopla.co.uk` search URL. |
| **Normalized Property & Agent Fields** | Captures `GBP` price, bedrooms, bathrooms, floor area, full address, coordinates, high-res photos, and agent details. |

---

## 📥 How to Use

1. Click **Try for free**
2. Paste one or more `zoopla.co.uk` search URLs into **Start URLs** (for example: `https://www.zoopla.co.uk/for-sale/property/london/`)
3. Set **Max Results** to choose how many listings to extract
4. Click **Start**
5. Export your dataset in **Excel, CSV, or JSON**

---

## 📤 Example Output

```json
{
  "id": "prop-948271",
  "portal": "zoopla.co.uk",
  "country": "United Kingdom",
  "currency": "GBP",
  "title": "Modern 3-Bedroom Residence in London",
  "price": 485000,
  "price_formatted": "GBP 485,000",
  "bedrooms": 3,
  "bathrooms": 2,
  "area": "132 m²",
  "address": "London, United Kingdom",
  "url": "https://www.zoopla.co.uk/for-sale/property/london/",
  "images": [
    "https://zoopla.co.uk/images/listing-948271-1.jpg"
  ],
  "scraped_at": "2026-10-16T00:00:00Z"
}
```

---

## ⚙️ Input Options

| Field | Description |
|---|---|
| **Start URLs** | One or more `zoopla.co.uk` search or property URLs to scrape |
| **Max Results** | Maximum number of property listings to collect per run (default: `40`) |

---

## 💰 Pricing & Free Tier

This Actor uses **Pay-Per-Result** pricing with a **`$0.00` start fee**:

| Apify Plan | Price per 1,000 Results | Per-Run Limit |
| :--- | :---: | :---: |
| **Free Plan** | **`$5.00 / 1K`** | Up to `40` results / run |
| **Starter (Bronze)** | **`$1.35 / 1K`** | Unlimited |
| **Scale (Silver)** | **`$0.95 / 1K`** | Unlimited |
| **Business+ (Gold / Platinum / Diamond)** | **`$0.75 / 1K`** | Unlimited |

> 💡 **Predictable, All-Inclusive Pay-Per-Event Pricing:** There is a **`$0.00` run start fee** and **no separate proxy configuration required**. You only pay the flat per-result rate above for data successfully delivered to your dataset — works out of the box on both **Free** and **Paid** Apify plans.

<!-- STORE_CROSS_REF_START -->
---

## 🔗 Related Actors from Our Store

Combine this Actor with our other **`128 MB` Pay-Per-Event (PPE)** tools in the same workflow (`$0.00` start fee):

| Related Actor | Best For | Starting Price |
| :--- | :--- | :--- |
| **[🏡 Zillow Search Scraper](https://apify.com/misterkhan/zillow-scraper)** | US homes for sale, rentals & sold listings — prices, Zestimates, beds/baths & coordinates | **From 💰`$0.90 / 1K`** |
| **[🇪🇸 Idealista Property Scraper](https://apify.com/misterkhan/idealista-scraper)** | Spain, Italy & Portugal real estate listings — prices in EUR, m², rooms & photos | **From 💰`$0.75 / 1K`** |
| **[🇫🇷 PAP.fr France FSBO Property Scraper](https://apify.com/misterkhan/pap-fr-particuliers-scraper)** | Owner-direct (Particulier à Particulier) property sales & rentals across France | **From 💰`$0.75 / 1K`** |

👉 **[See all Actors by `misterkhan` on Apify Store →](https://apify.com/misterkhan)**
<!-- STORE_CROSS_REF_END -->
---

## ❓ Frequently Asked Questions

**🛡️ Do I need to configure proxies to use this Actor? <br>**
**No — everything works out of the box with zero setup.** Regional routing, session management, and anti-blocking are handled automatically so you do not need to configure custom proxy settings.

---

## ⚠️ Disclaimer

This Actor collects publicly available property listing data from `zoopla.co.uk` for market research, valuation, and analytics purposes and is not affiliated with or endorsed by Zoopla UK Property.

## Your feedback

We keep this Actor under active maintenance. If a run finishes successfully but returns fewer results than you expected, hangs, or errors — please **open an Issue before posting a public review** so we can diagnose and fix it for you.

**🛠️ How to report** — Use the Actor’s [Issues tab](https://apify.com/misterkhan/zoopla-scraper/issues/open) in Apify Console. Include the run ID, your input JSON, and what you expected vs. what you got. <br>
**⏱️ Response time** — We aim to reply within 24 hours on business days. <br>
**⭐ Reviews** — Happy with the results? A short positive review helps other users find a reliable scraper. Ran into a problem? Open an Issue first — we’ll work with you to resolve it before you leave a rating. <br>


---

## 🛡️ Architecture & Engine Reliability

This scraper runs on the **[Crawlomatic Engine](https://crawlomatic.com)**:
- **Zero Proxy Configuration:** Intelligent residential and datacenter proxy rotation with automated regional ccTLD binding.
- **WAF Bypass Engine:** Autonomous challenge solving for Cloudflare Turnstile, DataDome, PerimeterX, Kasada, and Akamai.
- **Pay-Per-Event (PPE) Pricing:** Transparent pay-as-you-go pricing with \$0 starting fee.

## 📄 License

Apache License 2.0. See [LICENSE](LICENSE) for details.

Developed & Maintained by **[Crawlomatic](https://crawlomatic.com)**.
