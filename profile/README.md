<div align="center">
  <img src="https://proofio.app/whitelogo.png" alt="Proofio" width="120" style="border-radius:20px" />
  <h1>Proofio</h1>
  <p><strong>Turn customer reviews into your competitive advantage.</strong></p>
  <a href="https://proofio.app"><img src="https://img.shields.io/badge/proofio.app-→-6366f1?style=flat-square" alt="Website" /></a>
  <a href="https://app.proofio.app"><img src="https://img.shields.io/badge/Dashboard-→-6366f1?style=flat-square" alt="Dashboard" /></a>
  <a href="https://www.npmjs.com/package/proofio-sdk"><img src="https://img.shields.io/npm/v/proofio-sdk?style=flat-square&color=6366f1" alt="npm" /></a>
  <a href="mailto:support@proofio.app"><img src="https://img.shields.io/badge/support%40proofio.app-→-6366f1?style=flat-square" alt="Email" /></a>
</div>

---

## What is Proofio?

Proofio is an **Enterprise Review Intelligence Platform** that aggregates customer reviews from every major platform — App Store, Google Play, Trustpilot, Google Maps, G2, Yelp, Facebook, and more — into a single dashboard powered by AI.

Instead of manually checking eight different review platforms every week, Proofio brings everything together, analyzes it automatically, and surfaces the insights that actually matter: which features users love, what's driving rating drops, and where to focus your next sprint.

---

## What we build

| Repo | Description |
|---|---|
| `proofio-integrations` | Official examples, SDKs, and integration guides |
| `proofio-sdk` | TypeScript/JavaScript SDK (`npm install proofio-sdk`) |

---

## Core Features

**Review aggregation**
Connect App Store, Google Play, Trustpilot, Google Maps, G2, Yelp, Facebook, or import CSV files. Proofio ingests reviews automatically on a schedule.

**AI-powered insights**
Every review is analyzed for sentiment, emotion, topic, and language. Proofio clusters related reviews into themes (e.g. "Battery Life", "Onboarding", "Customer Support") and surfaces AI-generated summaries.

**Trend detection & alerts**
Proofio monitors your ratings over time and fires alerts when anomalies are detected — unusual sentiment spikes, sudden rating drops, or keyword surges.

**Automated reports**
Weekly and monthly PDF reports are generated automatically and emailed to your team every Monday morning.

**Developer API & SDK**
Every project exposes a public REST API and a TypeScript SDK. Use it to embed reviews on your website, feed data into your own dashboards, or build custom integrations.

**Embeddable widgets**
Drop a reviews grid, carousel, testimonials block, or rating badge onto any website — HTML, React, Next.js, WordPress, Shopify, Webflow, and Wix all supported.

---

## Quick Start

```bash
npm install proofio-sdk
```

```ts
import { ProofioClient } from "proofio-sdk";

const proofio = new ProofioClient({ apiKey: "YOUR_API_KEY" });

// Latest 10 positive reviews
const reviews = await proofio.reviews.list({ limit: 10, sentiment: "positive" });

// Aggregated stats
const stats = await proofio.aggregations.get();
console.log(`${stats.averageRating}★ across ${stats.totalReviews} reviews`);

// AI topic clusters
const clusters = await proofio.clusters.list();
```

Get your API key at [app.proofio.app](https://app.proofio.app) → Project → Settings → API.

---

## API Overview

**Base URL:** `https://api.proofio.app/api/v1/public`

| Endpoint | Description |
|---|---|
| `GET /reviews` | Paginated reviews with filters (sentiment, rating, language, source) |
| `GET /aggregations` | Total reviews, average rating, sentiment & rating distributions |
| `GET /clusters` | AI-generated topic clusters with keywords and sentiment scores |

**Authentication:** `x-api-key` header
**Rate limits:** 300 – 100,000 requests/month depending on plan

```bash
curl https://api.proofio.app/api/v1/public/reviews \
  -H "x-api-key: YOUR_API_KEY"
```

---

## Review Sources

<table>
<tr>
  <td align="center">App Store</td>
  <td align="center">Google Play</td>
  <td align="center">Trustpilot</td>
  <td align="center">Google Maps</td>
</tr>
<tr>
  <td align="center">G2</td>
  <td align="center">Yelp</td>
  <td align="center">Facebook</td>
  <td align="center">CSV Import</td>
</tr>
</table>

---

## Pricing

| Plan | Price | Projects | Sources | Reviews/month | API Requests |
|---|---|---|---|---|---|
| **Starter** | Free | 1 | 2 | 100 | 300 |
| **Growth** | $39/mo | 5 | 5 per project | 5,000 | 10,000 |
| **Scale** | $199/mo | 15 | 15 | 25,000 | 50,000 |

[See full pricing →](https://proofio.app/pricing)

---

## Tech Stack

Built with **Next.js**, **TypeScript**, **Firebase**, **OpenAI**, and **Stripe**. Deployed on **Vercel**.

---

## Links

- [Website](https://proofio.app)
- [Dashboard](https://app.proofio.app)
- [Integration Examples](https://github.com/Proofio-LLC/proofio-integrations)
- [npm Package](https://www.npmjs.com/package/proofio-sdk)
- [Twitter / X](https://twitter.com/proofioapp)
- [Support](mailto:support@proofio.app)

---

<div align="center">
  <sub>Built with care by the Proofio team · <a href="https://proofio.app">proofio.app</a></sub>
</div>
