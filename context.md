# Project Context: Clothing Brand Website

## Stack Constraints (STRICT — Do not deviate)
- **HTML + Tailwind CSS only.**
- No React, Vue, Angular, or any JavaScript framework.
- No component libraries (e.g., shadcn, MUI, Bootstrap).
- No TypeScript or JSX.
- Use semantic HTML5 elements for accessibility and SEO (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`, `<article>`, etc.).

---

## Project Overview
A multi-page website for a clothing brand. SEO best practices and modern visual design are priorities. All pages share a common navbar and footer.

---

## Shared Components (used on every page)

### Navbar (Top Bar)
- Brand logo (left-aligned)
- Search bar (centered or inline)
- User account menu (right-aligned: login/account icon)
- Responsive: collapses to a hamburger menu on mobile

### Footer
Divided into three sections:
1. **Categories**: Footwear, Shirts, Pants, Accessories
2. **Legal**: Terms and Conditions, Privacy Policy, About the Brand
3. **Contact**: email, social links, or contact form link

---

## Pages

### 1. Home (`index.html`)
**SEO**: `<title>`, `<meta name="description">`, Open Graph tags, semantic headings.

**Sections (top to bottom):**
1. Navbar (shared)
2. **Hero** — full-width or large banner highlighting a special product or brand campaign. Include a clear CTA button (e.g., "Shop Now").
3. **New Arrivals** — horizontal scrollable or row-based product card list.
4. **Best Sellers** — same card layout as New Arrivals.
5. Footer (shared)

**Product Card layout:**
- Product image (with `alt` text)
- Product name
- Price
- Optional: quick "Add to Cart" link

---

### 2. Catalog (`catalog.html`)
**SEO**: unique `<title>` and `<meta name="description">`.

**Layout:**
1. Navbar (shared)
2. **Filter Bar** (above the grid):
   - Filter by Category (dropdown or pill buttons)
   - Filter by Size (dropdown or pill buttons)
3. **Product Grid**: 4 columns × 5 rows = 20 product cards visible as reference
4. Footer (shared)

---

### 3. Product View (`product.html`)
**SEO**: unique `<title>` with product name, `<meta name="description">`, structured data hint in comments.

**Layout:**
1. Navbar (shared)
2. **Two-column layout** (50/50 split on desktop, stacked on mobile):
   - **Left column**: Large product image
   - **Right column**:
     - Product name (`<h1>`)
     - Reference/code (small text)
     - Size selector (e.g., S, M, L, XL as buttons or `<select>`)
     - Price (prominent)
     - Quantity selector (number input or +/− buttons)
     - "Add to Cart" button (primary CTA)
3. **Detail section** (below the two columns, full width):
   - Materials
   - Recommended use / wear scenarios
4. Footer (shared)

---

### 4. Cart (`cart.html`)
**Full-page cart view** — not a sidebar or drawer.

**Layout:**
1. Navbar (shared)
2. **Product List** (left or top portion):
   - Each row: thumbnail, product name, unit price, quantity, total per product, remove button
   - Include **3 sample/placeholder products** to demonstrate the visual behavior
3. **Order Summary box** (right column on desktop, below list on mobile):
   - Subtotal
   - Tax
   - Total
   - "Proceed to Checkout" button
4. Footer (shared)

---

### 5. Checkout (`checkout.html`)
**Multi-step form** — 3 steps displayed sequentially (use `<section>` or `<fieldset>` with Tailwind step indicators).

**Steps:**
1. **Personal Details**: full name, email, phone
2. **Shipping Address**: street, city, state/province, postal code, country
3. **Card Payment**: cardholder name, card number, expiry date, CVV

**Notes:**
- Display a step progress indicator at the top (Step 1 / 2 / 3)
- Each step fits within the page — no full-page reloads needed for visual reference; steps can be separate visible sections or toggled via minimal JS
- Form fields must use proper `<label>` elements for accessibility

---

## Design Guidelines
- **Style**: Modern, clean, minimal — large imagery, generous whitespace, bold typography.
- **Color palette**: Define a brand primary color (e.g., black or deep navy) with neutral backgrounds and accent highlights. Use Tailwind's color utilities.
- **Typography**: Use a Google Font (loaded via `<link>` in `<head>`) — e.g., Inter or Playfair Display.
- **Responsive**: Mobile-first. Use Tailwind breakpoints (`sm:`, `md:`, `lg:`).
- **Images**: Use placeholder images (e.g., `https://placehold.co/`) with descriptive `alt` attributes.
- **SEO**: Each page has a unique `<title>`, `<meta name="description">`, and uses semantic HTML heading hierarchy (`h1` → `h2` → `h3`).

---

## File Structure Reference
```
index.html        → Home page
catalog.html      → Product catalog with filters
product.html      → Single product detail view
cart.html         → Shopping cart
checkout.html     → Checkout / payment form
```

---

## Out of Scope (do not include)
- Backend logic or server-side code
- Databases or API calls
- Authentication flows beyond visual UI
- React, Vue, Angular, or any JS framework
- CSS preprocessors (Sass, Less)
