# PShop Solar - AI Agent Instructions

This document provides essential context for AI agents working with the PShop Solar e-commerce website codebase.

## Project Overview

PShop Solar is a bilingual (Khmer/English) e-commerce website specializing in solar equipment sales, particularly focusing on water pumps and related solar products.

### Key Files and Structure

- `index.html` - Main landing page with navigation and search
- `product.html` - Product listing page
- `product-detail.html` - Individual product details
- `script.js` - Core JavaScript functionality and product data
- `style.css` - Main stylesheet
- `product.css` - Product-specific styles

## Data Structure Patterns

Products are defined in `script.js` using a consistent structure:

```javascript
{
    id: number,
    title: string, // Product name in Khmer
    description: string, // Brand and specs in Khmer
    imgSrc: string, // Path to product image
    Info: [{ // Optional detailed specifications
        brand: string,
        model: string,
        size: string,
        horsepower: string,
        dc: string,
        ac: string,
        heigh: string,
        amountwater: string,
        solarpanel: string
    }]
}
```

## Image Organization

Images are organized by product category in the `image/` directory:
- `s_pump_*` - Submersible pumps by brand (Veichi, Fielben, Hippo)
- `T_pump_*` - Tank pumps by brand (Topsun, Feilben)

## Localization Approach

- Khmer text uses Unicode directly in the strings
- Font family for Khmer text is controlled via CSS variable `--khmer-font`
- Product titles and descriptions are in Khmer by default

## UI Components

- Header with contact information (phone numbers and location)
- Navigation bar with logo, menu items, and search
- Product cards with consistent layout and styling
- Responsive design breakpoints defined in CSS

When making changes:
1. Maintain bilingual support
2. Follow existing product data structure
3. Use appropriate image directory structure
4. Preserve responsive design patterns

For new features:
1. Match existing bilingual patterns
2. Follow established component styling
3. Maintain mobile-friendly layouts