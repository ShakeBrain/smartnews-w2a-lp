# SmartNews W2A LP Prototypes

Web-to-App landing page prototypes for the SmartNews PoC (2026-08).

## Live URL

- Default: https://shakebrain.github.io/smartnews-w2a-lp/
- Production (planned): https://lp.smartnews.com/

## Structure

```
├── index.html                LP 一覧
├── gardening.html            Topic Hub 型 (mint)
├── fantasy-football.html     Topic Hub 型 (red)
├── celebrity-gossip.html     Topic Hub 型 (orange)
├── coffee.html               Topic Hub 型 (blue)
├── politics.html             Diverse Perspectives 型 (ink)
├── _shared.css               brand-aligned design tokens
├── _lp.js                    Google Sheet -> article-list 動的更新
└── assets/                   公式 SmartNews ロゴ
```

## データフロー

```
Meta Catalog "last_72h_all_articles" (55K products)
    -> populate_sheet_from_meta.py (別 repo で管理)
    -> Google Sheet (中間 buffer, 4 tab)
    -> LP が gviz CSV endpoint から fetch
    -> article-list に real 記事表示
```

## Build / Deploy

Build 不要 (pure HTML/CSS/JS)。GitHub Pages で `main` branch 直接配信。
