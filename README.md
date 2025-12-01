# Depop Scraper

![Depop Scraper](https://i.ibb.co/35v5RGGF/Screenshot-2025-10-25-at-11-50-16-PM.png)

This Apify actor allows you to scrape product listings from Depop.com, the leading social marketplace for secondhand fashion. Extract comprehensive product data including prices, descriptions, seller information, and images — perfect for resale market research, fashion trend analysis, and competitive intelligence.

<p align="center">
  <img src="https://apify-image-uploads-prod.s3.us-east-1.amazonaws.com/DevbkY3adMTBuoECt-actor-N45rtnTadExuILiYC-LDUHuCSWz0-idss78PWdJ_1761983889885.jpeg" alt="Depop Scraper" style="height: 60px; margin-right: 15px;" /><a href="https://apify.com/lexis-solutions/depop-scraper" target="_blank">
    <img src="https://img.shields.io/badge/Try%20it%20on-Apify-0066FF?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDA4IiBoZWlnaHQ9IjQwOCIgdmlld0JveD0iMCAwIDQwOCA0MDgiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF8zNDFfNDE1NykiPgo8cGF0aCBkPSJNMjE4LjY5NSAxMDRIMzAwLjk3QzMwMi42NDMgMTA0IDMwNCAxMDUuMzU3IDMwNCAxMDcuMDNWMjMyLjc2NkMzMDQgMjM1Ljc3OCAzMDAuMDgzIDIzNi45NDUgMjk4LjQzNCAyMzQuNDI1TDIxNi4xNTkgMTA4LjY5QzIxNC44NDEgMTA2LjY3NCAyMTYuMjg3IDEwNCAyMTguNjk1IDEwNFoiIGZpbGw9IndoaXRlIi8+CjxwYXRoIGQ9Ik0xODkuMzA1IDEwNEgxMDcuMDNDMTA1LjM1NyAxMDQgMTA0IDEwNS4zNTcgMTA0IDEwNy4wM1YyMzIuNzY2QzEwNCAyMzUuNzc4IDEwNy45MTcgMjM2Ljk0NSAxMDkuNTY2IDIzNC40MjVMMTkxLjg0IDEwOC42OUMxOTMuMTU5IDEwNi42NzQgMTkxLjcxMyAxMDQgMTg5LjMwNSAxMDRaIiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNMjAyLjU5MSAyMDQuNjY4TDEwOS4xMjcgMjk4LjgzNUMxMDcuMjI5IDMwMC43NDcgMTA4LjU4MyAzMDQgMTExLjI3OCAzMDRIMjk2LjhDMjk5LjQ4MyAzMDQgMzAwLjg0MiAzMDAuNzcgMjk4Ljk2NyAyOTguODUyTDIwNi45MDggMjA0LjY4NUMyMDUuNzI2IDIwMy40NzUgMjAzLjc4MiAyMDMuNDY4IDIwMi41OTEgMjA0LjY2OFoiIGZpbGw9IndoaXRlIi8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDBfMzQxXzQxNTciPgo8cmVjdCB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEwNCAxMDQpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==&logoColor=white" alt="Try it on Apify" style="border-radius: 12px; height: 60px;" />
  </a>
</p>


---


## 📊 Actor Stats

| Stat | Value |
|------|-------|
| **Version** | `0.1.2` |
| **Last Update** | Dec 1, 2025 |

---



## 💻 Integration Examples

This repository includes example code showing how to integrate the `depop-scraper` actor into your projects.

You can find example implementations in the [`examples/`](./examples) folder:
- **TypeScript/JavaScript**: See [`examples/typescript/`](./examples/typescript) for a complete TypeScript example
- **Python**: See [`examples/python/`](./examples/python) for a complete Python example

Each example includes:
- Ready-to-use code templates
- Setup instructions
- Documentation links

---


## 🚀 Key Features

- 🔎 Scrape listings from Depop search pages or individual product detail pages
- 👕 Comprehensive product data (title, description, brand, category, condition)
- 💰 Accurate pricing extraction with currency support
- 📸 High-resolution product image URLs extraction
- 👤 Seller information (username, rating, location, shop URL)
- 💖 Engagement metrics (likes, saves, views)

---

## 👥 Who Is This Actor Suitable For?

- 🛍️ Resellers and thrift store owners
- 📈 Fashion market researchers and analysts
- 🧠 Data scientists studying secondhand fashion trends
- 🧰 Developers building fashion search platforms
- 📚 E-commerce intelligence teams
- 💼 Brand managers monitoring resale markets
- 📊 Pricing optimization specialists

---

## 📥 Input Schema

The actor accepts the following input parameters:

### Search Page URLs

```json
{
  "startUrls": [
    {
      "url": "https://www.depop.com/search/?q=lululemon+define+jacket"
    },
    {
      "url": "https://www.depop.com/products/username-lululemon-define-jacket/",
    }
  ],
  "maxItems": 100,
  "proxyConfiguration": {
    "useApifyProxy": true,
    "apifyProxyGroups": ["RESIDENTIAL"],
    "apifyProxyCountry": "GB"
  }
}
```

### Input Parameters

- **startUrls** (required): Array of Depop URLs to scrape. Supports both:
- **maxItems** (optional): Maximum number of products to scrape (default: 10)
- **proxyConfiguration**: Proxy settings for anonymous scraping (recommended: RESIDENTIAL, GB)

---

## 📤 Output Schema

Each scraped product returns comprehensive structured data:

```json
[
  {
    "id": "bsells027-black-and-gold-lululemon-define-e851",
    "slug": "bsells027-black-and-gold-lululemon-define-e851",
    "url": "https://www.depop.com/products/bsells027-black-and-gold-lululemon-define-e851/",
    "title": "Black and gold Lululemon Define Jacket",
    "description": "Black and gold Lululemon Define Jacket size 6. Excellent condition, worn only a few times. Features thumb holes and zipper pockets. No flaws or pilling.",
    "price": "85",
    "currency": "USD",
    "status": "ONSALE",
    "brand": "Lululemon",
    "images": [
      "https://media-photos.depop.com/b1/12345678/1234567890_abc123def456/P0.jpg",
      "https://media-photos.depop.com/b1/12345678/1234567890_abc123def456/P1.jpg",
      "https://media-photos.depop.com/b1/12345678/1234567890_abc123def456/P2.jpg"
    ],
    "dateCreated": "2025-01-24T18:30:00.000Z",
    "country": "US"
  },
  {
    "id": "vintage-shop-90s-nike-windbreaker-xl",
    "slug": "vintage-shop-90s-nike-windbreaker-xl",
    "url": "https://www.depop.com/products/vintage-shop-90s-nike-windbreaker-xl/",
    "title": "Vintage 90s Nike Windbreaker XL",
    "description": "Authentic vintage Nike windbreaker from the 90s. Size XL. Great condition with minor wear consistent with age. Classic colorway.",
    "price": "45",
    "currency": "USD",
    "status": "ONSALE",
    "brand": "Nike",
    "images": [
      "https://media-photos.depop.com/b1/98765432/0987654321_xyz789abc123/P0.jpg"
    ],
    "dateCreated": "2025-01-23T14:20:00.000Z",
    "country": "US"
  }
]
```

### Output Fields Explained

- **id**: Unique product identifier
- **slug**: URL-friendly product identifier
- **url**: Direct link to the product page
- **title**: Product title/name
- **description**: Full product description
- **price**: Product price (numeric string)
- **currency**: Currency code (USD, GBP, EUR, etc.)
- **status**: Product availability (ONSALE, SOLD)
- **brand**: Product brand/designer
- **images**: Array of high-resolution product image URLs
- **dateCreated**: Timestamp when data was scraped
- **country**: Seller's country code

---

## 🎯 Use Cases

### 1. Resale Market Research
Track pricing trends for specific brands and categories to optimize your sourcing and pricing strategy.

### 2. Competitive Intelligence
Monitor competitor listings, pricing strategies, and product descriptions to stay ahead in the market.

### 3. Fashion Trend Analysis
Identify emerging fashion trends by analyzing popular items, brands, and styles on Depop.

### 4. Pricing Optimization
Compare prices across similar items to position your listings competitively.

### 5. Inventory Planning
Discover what products are in high demand to inform your sourcing decisions.

### 6. Brand Monitoring
Track how your brand or products are being resold on the secondhand market.


## 📞 Support & Feedback

Got feedback or need an extension?

Lexis Solutions is a [certified Apify Partner](https://apify.com/partners/find). We can help you with custom solutions or data extraction projects.

Contact us over [Email](mailto:scraping@lexis.solutions) or [LinkedIn](https://www.linkedin.com/company/lexis-solutions)

---

## 💝 Support Our Work

If you're happy with our work and scrapers, you're welcome to leave us a company review [here](https://apify.com/partners/find/lexis-solutions/review) and leave a review for the scrapers you're subscribed to. It will take you less than a minute but it will mean a lot to us!