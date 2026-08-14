# WordRunes Assets

Public game asset CDN for the WordRunes app.

This repo mirrors the app's local `/assets` folder structure. New artwork is
added here first (CDN-first), then the same PNG is bundled into the app on the
next build as the offline fallback. Catalog data (names, prices, rewards,
categories, image URLs) lives in the Supabase `shop_catalog` table — this repo
holds **only the asset PNG files**.

```
assets/
  icons/     # avatar/product artwork (mirrors app assets/icons)
  banners/   # future banner/background art (mirrors app assets/banners)
```

Resolution order in the app: bundled `require` → CDN `image_url` → fallback.

Base URL: **https://sitebytom.github.io/wordrunes-assets/**
