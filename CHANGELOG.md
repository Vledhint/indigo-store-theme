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
