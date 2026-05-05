# Changelog

All notable changes to the Indigo Store theme are documented here.

## [Unreleased] — 2026-04-21

### Added
- `snippets/ticker.liquid` — reusable seamlessly looping ticker banner (dark/blue themes)
- `snippets/product-card.liquid` — product card with image, CARRITO/COMPRAR buttons, color swatches
- `sections/kids-section.liquid` — Kids landing page with hero, NIÑA/NIÑO tickers, age-range grid
- Montserrat font (weights 400, 700, 800, 900) loaded via Google Fonts in `layout/theme.liquid`

### Changed
- `sections/header.liquid` — full redesign: sticky navy header, centered INDIGO STORE logo, nav links left, search/account/cart icons right
- `sections/home.liquid` — full redesign matching Figma: hero, features bar, men/women/kids product grids with tickers, tagline section, REBAJAS sale section
- `sections/footer.liquid` — full redesign: black background, 3-column link layout (Términos / Información / Políticas)
- `sections/collection.liquid` — redesigned with ticker header, filter bar, 4-column product grid, pagination
- `sections/product.liquid` — redesigned with 2×2 image gallery, sticky info panel, color swatches, size selector, CARRITO/COMPRAR buttons, accordion sections
- `sections/cart.liquid` — redesigned with CARRITO ticker, quantity controls, order totals, PAGAR PEDIDO button
- `sections/special-grid.liquid` — converted to gender/category landing page with hero + configurable mosaic category tiles
- `locales/en.default.json` — added translation keys for cart totals, product actions, customer auth, and section labels
- `assets/critical.css` — added CSS reset, global button system, layout utilities
- `config/settings_schema.json` — changed default font from `work_sans_n4` to `montserrat_n4`

### Refactored — 2026-04-21 (Tailwind CSS migration)
- `snippets/ticker.liquid` — replaced custom stylesheet with Tailwind classes; kept only keyframe animation and hover-pause in `{% stylesheet %}`
- `snippets/product-card.liquid` — fully replaced custom CSS with Tailwind utilities; image hover scale uses `group`/`group-hover` pattern
- `sections/header.liquid` — replaced all custom CSS with Tailwind; sticky positioning, flex layout, cart badge, and icon sizing via utilities
- `sections/footer.liquid` — removed `{% stylesheet %}` entirely; 3-col responsive grid via `grid-cols-3 sm:grid-cols-1`
- `sections/home.liquid` — removed `{% stylesheet %}` entirely; all layout, spacing, typography, and responsive breakpoints via Tailwind; `clamp()` font sizes via arbitrary values
- `sections/collection.liquid` — replaced custom CSS with Tailwind; kept only `{% stylesheet %}` for Shopify-generated pagination HTML
- `sections/product.liquid` — replaced custom CSS with Tailwind; kept `{% stylesheet %}` for `details/summary` marker reset, sticky panel height calc, and Shopify payment button overrides
- `sections/cart.liquid` — replaced custom CSS with Tailwind; removed separate qty-control stylesheet, inline Tailwind on all elements
- `sections/special-grid.liquid` — replaced custom CSS with Tailwind; kept only `{% stylesheet %}` for dynamic `grid-column/grid-row span` classes (Liquid-interpolated values not scannable by Tailwind)

**Responsive breakpoints applied across all sections:**

| Breakpoint | Width | Usage |
|---|---|---|
| `lg:` | ≤ 1024px | Product page stacks, 3-col grids |
| `md:` | ≤ 768px | 2-col grids, category mosaic |
| `sm:` | ≤ 640px | 1-col footer/sale, 2-col products, reduced padding |
