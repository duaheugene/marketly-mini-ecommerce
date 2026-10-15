# Marketly — Mini E-Commerce Product Page

A responsive, frontend-first e-commerce demo built with semantic HTML, custom CSS, and vanilla JavaScript. Created to cover the mini e-commerce assignment requirements while presenting a more complete portfolio-quality shopping experience.

## Run it

**Recommended:** open this folder in VS Code and run `index.html` with the Live Server extension. You can also serve the folder with Python:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

The app attempts to fetch product data from [Fake Store API](https://fakestoreapi.com/products). If the API is offline or unavailable, it automatically uses a bundled sample catalogue. Google Fonts and product photography use external URLs, so an internet connection improves the visual experience. The core interface and fallback product data are local.

## Features

- Responsive storefront for desktop, tablet, and mobile
- Product catalogue with API loading and local fallback
- Search by product title
- Category filters and maximum-price slider
- Sorting by featured, price, rating, and name
- Product detail quick-view modal
- Saved products / favourites
- Shopping bag with quantity changes, removal, subtotal, shipping estimate, free-shipping progress, and total
- Checkout form with required fields, email, phone, minimum-length, region, and terms validation
- Demo order confirmation with order ID; orders are stored in browser local storage
- Newsletter form validation and local demo subscription storage
- Cart and favourites persist in local storage
- Keyboard shortcut Ctrl/Cmd + K to focus search, Escape to close overlays, accessible labels, reduced-motion support

## Assignment checklist

1. **Product listing/catalogue, search, category filtering:** `renderProducts`, `filteredProducts`, `setCategory` in `app.js`.
2. **Shopping cart, add/remove, total:** `addToCart`, `updateQuantity`, `renderCart` in `app.js`.
3. **Mock API:** `loadProducts` fetches Fake Store API and falls back to bundled demo products.
4. **Form validation:** `validateField` and `submitOrder` validate checkout fields; newsletter form validates email.

## Important demo limitations

- This is a frontend demo, not a production commerce backend.
- Checkout creates a demo order in the current browser only. No payment is taken, and no order is sent to a fulfilment system.
- The payment selector is illustrative. Do not collect real customer payment details with this demo.
- API product prices are converted from USD using a fixed illustrative rate for display in GH₵. It is not a live exchange rate.
- A production release should add a backend, server-side validation, real inventory/order persistence, authentication if needed, privacy/terms pages, and a trusted payment provider integration.

## Project structure

```text
marketly-store/
├── index.html
├── styles.css
├── app.js
└── README.md
```
