# 🔍 WackyFlip-SEO

**Tools & Metadata Services for Discoverability**

This repository powers the infrastructure that makes **[WackyFlip.com](https://wackyflip.com)** and its games discoverable across search engines, social platforms, and app directories.

`WackyFlip-SEO` includes metadata generators, sitemap builders, structured data schemas, Open Graph tools, and automation scripts to boost **organic traffic**, **shareability**, and **platform indexing**.

---

## 🎯 Purpose

Wacky Flip is a fast-growing casual game platform. This repo ensures that:

* Players can **easily find games via Google or Bing**
* Game pages are **social media friendly**
* New content is **indexed immediately**
* Metadata is **automatically generated** across updates

---

## ✨ Key Features

| Feature                       | Description                                                              |
| ----------------------------- | ------------------------------------------------------------------------ |
| 🗺️ Dynamic Sitemap Generator | Builds updated XML sitemaps for all games, tags, and blog entries        |
| 🧠 Meta Tag Injection         | Adds dynamic Open Graph & Twitter Card tags for every game page          |
| 📊 Google Search Console Feed | Automated pinging to GSC for new content and sitemap changes             |
| 📘 Schema Markup              | Adds JSON-LD for games, articles, reviews, and product-like rich results |
| 🔁 Robots.txt & Meta Robots   | Configurable indexing rules and canonical URLs for duplicate pages       |
| 📦 Integration with CMS       | Syncs metadata from `WackyFlip-CMS` or `WackyFlip-ContentPipeline`       |

---

## 🛠 Tech Stack

* Node.js (TypeScript)
* Cheerio / React DOM parsing
* Google Search Console API
* XML & JSON-LD generators
* Used alongside Next.js or static site builds

---

## 📁 Suggested Directory Structure

```
WackyFlip-SEO/
├── scripts/
│   ├── generate-sitemap.ts
│   ├── push-to-gsc.ts
│   └── inject-meta-tags.ts
├── templates/
│   ├── opengraph.tsx
│   ├── twitter-card.tsx
│   └── schema-game.ts
├── configs/
│   └── robots.config.json
├── tests/
├── README.md
```

---

## ⚙️ Sample Usage

```ts
import { generateMetaTags } from './scripts/inject-meta-tags';
import { getGameData } from './data/games';

const meta = generateMetaTags(getGameData("rainbow-obby"));
console.log(meta.title); // "Play Rainbow Obby | Wacky Flip"
```

---

## 📘 Example Output

### 🔖 Open Graph Tags

```html
<meta property="og:title" content="Play Slime Road | Wacky Flip">
<meta property="og:image" content="https://wackyflip.com/thumbs/slime-road.png">
<meta property="og:type" content="website">
<meta property="og:url" content="https://wackyflip.com/slime-road">
```

### 📑 JSON-LD Schema

```json
{
  "@context": "https://schema.org",
  "@type": "VideoGame",
  "name": "Gun Flip",
  "url": "https://wackyflip.com/gun-flip",
  "author": "Wacky Flip Studios",
  "applicationCategory": "Game",
  "operatingSystem": "Browser",
  "image": "https://wackyflip.com/assets/gun-flip-cover.png"
}
```

---

## 🔄 Integrations

* `WackyFlip-Web` – injects generated meta at build time
* `WackyFlip-Blog` – dynamic blog post SEO metadata
* `WackyFlip-ContentPipeline` – syncs new pages with sitemap updates
* `WackyFlip-Locale` – generates i18n-compatible SEO content

---

## 🧪 Roadmap

* [ ] Auto-generated preview thumbnails for social
* [ ] Metadata A/B testing (title/description variants)
* [ ] Bing Webmaster & Apple App Site Association
* [ ] Analytics hooks for measuring CTR via `WackyFlip-Stats`

---

## 🧑‍💻 Contributions

Want to optimize SEO for a specific game or regional market?
Open a PR with your enhancements or share suggestions via issues!

---

## 📜 License

MIT © 2025 Wacky Flip Studios
