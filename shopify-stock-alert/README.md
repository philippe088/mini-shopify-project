# Alerte de stock – Thème Liquid et application Shopify

## Pourquoi ce projet

Projet personnel réalisé pour apprendre Shopify, en reprenant la logique de mise à jour des stocks à partir de messages (déjà utilisée dans un projet précédent avec Azure) et en la reproduisant avec les outils Shopify.

## Fonctionnalités

- **Thème (Liquid) :** section « Produits vedettes » avec un badge « Plus que X en stock » quand l'inventaire est bas, et « Épuisé » à 0.
- **Application d'administration :** liste des produits en stock bas, seuil configurable, et journal des mises à jour reçues par webhook (`products/update`).

> Projet en cours de construction — voir l'avancement dans les commits.

## Technologies

Liquid · Shopify CLI · Skeleton theme · Theme Check · React Router 7 · TypeScript · Polaris · API Admin GraphQL · Webhooks · Prisma · SQLite

## Exécution locale

```powershell
# Thème
cd theme
shopify theme dev --store <ton-nom-de-boutique>

# Application
cd alerte-stock-app
shopify app dev
```
