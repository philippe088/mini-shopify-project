# Stock Alert – Liquid Theme and Shopify App

## Why this project

A personal project built to learn Shopify, reusing the same stock-update logic I had already implemented from messages in a previous project (on Azure), reproduced here with Shopify's own tools.

## Features

- **Theme (Liquid):** a "Premium Products" section with an "Only X in stock" badge when inventory is at or below a configurable threshold, and "No stock" at 0.
- **Admin app:** lists low-stock products, a configurable threshold, and a log of updates received via webhook (`products/update`).

> Project under construction — see progress in the commits.

## Screenshots

The store is a private development store, so here is what it looks like.

**Premium Products section on the home page:** the "No stock" badge (0 units) and the "Only 3 in stock" badge (3 units, threshold of 5).

![Premium Products section with stock badges](shopify-stock-alert/docs/screenshots/home.png)

**Configurable threshold in the theme editor:** the same product with 3 units in stock, before and after changing "Low Product Threshold".

| Threshold 5: stock is below it, badge shown | Threshold 2: stock is above it, no badge |
|---|---|
| ![Threshold set to 5](shopify-stock-alert/docs/screenshots/below-threshold.png) | ![Threshold set to 2](shopify-stock-alert/docs/screenshots/above-threshold.png) |

**Inventory in the Shopify admin:** the badges come from real inventory data (`Liquid`: 3 in stock, `Multi-managed`: 0 in stock).

![Products page in the Shopify admin](shopify-stock-alert/docs/screenshots/products-admin-page.png)

## Technologies

Liquid · Shopify CLI · Skeleton theme · Theme Check · React Router 7 · TypeScript · Polaris · Admin GraphQL API · Webhooks · Prisma · SQLite

## Running locally

```powershell
# Theme
cd shopify-stock-alert/theme
shopify theme dev --store <your-store-name>

# App
cd shopify-stock-alert/alerte-stock-app
shopify app dev
```
