# After Inked — Shopify Storefront Customization & Bundle Collection Improvements

**Professional client project | My Amazon Guy (MAG)**  
**Role:** Shopify Developer — Storefront customization, responsive fixes, and bundle collection cleanup  
**Platform:** Shopify  
**Technologies:** Shopify Liquid, HTML, CSS, Shopify Theme Editor  
**Website:** [After Inked](https://afterinked.com/)

## Project Overview

After Inked is a tattoo and piercing aftercare storefront. During my work at My Amazon Guy (MAG), I worked on Shopify storefront changes associated with its **Bundle & Save** collection, focusing on product-card purchase controls, responsive styling, and a more consistent shopping experience.

This repository documents selected aspects of that professional work through storefront screenshots and technical implementation notes. It is **not a complete Shopify theme** and does not claim that I authored the existing theme or every element visible in the screenshots.

## Development Highlights

### 1. Bundle & Save collection — purchase controls

**Relevant theme snippet:** `snippets/card-product.liquid`

The collection-specific product card implementation:

- Checks whether the active collection handle is `bundle-and-save`.
- Displays **Add to Cart** and **Checkout Now** directly on eligible, available, single-variant product cards.
- Uses the selected or first available variant ID for the add-to-cart action.
- Provides a direct checkout form using Shopify's cart-add route and a checkout return path.
- Shows a **View product** fallback when the product does not meet the direct-purchase conditions.
- Avoids displaying the usual quick-buy control in addition to the bundle-specific purchase controls.

These behaviors are implemented within the existing storefront theme rather than as a standalone app.

### 2. Responsive bundle-card buttons

**Relevant stylesheet:** `assets/component-card.css`

The bundle card CSS:

- Keeps both purchase buttons visible and arranged vertically.
- Uses full-width controls with consistent spacing and minimum touch-friendly heights.
- Applies width constraints and `box-sizing: border-box` to prevent horizontal overflow.
- Adjusts padding and font size at narrower viewport widths.

The relevant bundle-specific CSS is located near the end of the locally archived stylesheet (approximately lines 901–911 in the reviewed version).

### 3. Storefront presentation and QA

The captured storefront demonstrates:

- The **Bundle & Save** collection with product images, savings indicators, pricing, filters, and purchase controls.
- An aftercare bundle product detail page with one-time and subscription purchase options.
- An artist bundle product detail page with bundle pricing and subscription options.
- A responsive storefront presentation reviewed during the project.

Screenshots show the storefront as captured. They are evidence of the interface, not proof that every component pictured was independently developed by me.

## Storefront Screenshots

### Homepage — Hero

![After Inked homepage hero](<01 - Homepage/AfterInked_01_Homepage_Hero.png>)

### Bundle & Save — Collection

![After Inked Bundle & Save collection](<02 - Collection Pages/AfterInked_02_Bundle_Collection.png>)

### Aftercare Bundle — Product Detail Page

![Aftercare bundle product detail](<03 - Product Detail Pages/AfterInked_03_Aftercare_Bundle_PDP.png>)

### Aftercare Bundle — Purchase Options

![Aftercare bundle purchase options](<03 - Product Detail Pages/AfterInked_04_Aftercare_Bundle_Purchase_Options.png>)

### Artist Bundle — Product Detail Page

![Artist bundle product detail](<03 - Product Detail Pages/AfterInked_05_Artist_Bundle_PDP.png>)

## Repository Structure

```text
afterinked-shopify/
├── 01 - Homepage/
│   └── AfterInked_01_Homepage_Hero.png
├── 02 - Collection Pages/
│   └── AfterInked_02_Bundle_Collection.png
├── 03 - Product Detail Pages/
│   ├── AfterInked_03_Aftercare_Bundle_PDP.png
│   ├── AfterInked_04_Aftercare_Bundle_Purchase_Options.png
│   └── AfterInked_05_Artist_Bundle_PDP.png
└── README.md
```

**Code reference:** Full working copies of `component-card.css` and `card-product.liquid` have been preserved locally for documentation and review. They are not assumed to be cleared for public redistribution. Any public code examples should contain only material authorized for sharing, with the original theme's ownership and licensing respected.

## What This Project Demonstrates

- Working with an existing Shopify theme and understanding its Liquid component structure.
- Implementing collection-specific storefront behavior using Liquid conditionals and product/variant data.
- Coordinating Liquid markup with CSS for product-card interactions.
- Improving responsive layouts and touch-friendly purchase controls.
- Documenting production-oriented ecommerce development work with screenshots and implementation notes.

## Attribution & Scope

This work was undertaken as part of my Shopify Developer role at **My Amazon Guy (MAG)** for the **After Inked** client project. After Inked, MAG, the theme creator, and third-party providers retain their respective rights to brand assets, theme code, and other materials. The repository is a selected professional portfolio record, not an official client distribution or a complete, independently authored storefront.
