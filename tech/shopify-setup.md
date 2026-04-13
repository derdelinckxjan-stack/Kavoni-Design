# Shopify Setup — Kavoni Design

> Theme configuration, app stack, API notes, and store settings reference.

---

## Store Details

| Setting | Value |
|---|---|
| **Store URL** | kavonidesign.com |
| **Shopify plan** | *(add current plan)* |
| **Admin URL** | admin.shopify.com/store/kavonidesign |
| **Primary market** | Belgium |
| **Currency** | EUR |
| **Language** | NL (primary) / EN |

---

## Theme

| Setting | Detail |
|---|---|
| **Active theme** | *(add theme name — e.g. Dawn / custom)* |
| **Theme version** | *(add version)* |
| **Customised** | Yes — dark/gold brand colours applied |
| **Backup** | Always duplicate before editing |

### Brand Styling Applied
- Background: near-black (`#0D0D0D` range)
- Accent / CTA colour: gold (`#C9A84C` range)
- Typography: serif for headings, clean sans-serif for body
- Button style: sharp corners, gold fill or gold border
- Angular design language — avoid rounded/soft UI

### Theme Customisation Path
`Shopify Admin → Online Store → Themes → Customise`

Key sections customised:
- Header: logo + navigation
- Hero: video/image banner
- Product pages: BMW fitment metafields displayed
- Footer: newsletter signup form (Klaviyo embedded)

---

## Navigation Structure

```
Main menu:
├── Shop
│   ├── Aerodynamics
│   ├── Exhaust Systems
│   ├── Lighting
│   ├── Interior & Controls
│   └── Engine Bay
├── By Model
│   ├── E-Series →  E90, E92/93 M3
│   ├── F-Series →  F20, F22, F30, F80, F82, F87, ...
│   └── G-Series →  G20, G80, G82, G87, ...
├── About
└── Contact
```

---

## Collections

| Collection | Handle | Filter type |
|---|---|---|
| Aerodynamics | aerodynamics | Manual / smart (tag: category-aero) |
| Exhaust Systems | exhaust-systems | Smart (tag: category-exhaust) |
| Lighting | lighting | Smart (tag: category-lighting) |
| Interior & Controls | interior-controls | Smart (tag: category-interior) |
| Engine Bay | engine-bay | Smart (tag: category-engine-bay) |
| BMW 1 Series (F20) | bmw-1-series-f20 | Smart (tag: f20) |
| BMW M3 (F80) | bmw-m3-f80 | Smart (tag: f80) |
| *(add all model collections)* | | |

---

## Product Tags Convention

All products should be tagged consistently for smart collections and filtering:

| Tag type | Format | Example |
|---|---|---|
| Chassis code | lowercase | `f80`, `g80`, `e92` |
| Category | `category-[name]` | `category-aero`, `category-exhaust` |
| Model name | `model-[name]` | `model-m3`, `model-3-series` |
| Engine | `engine-[code]` | `engine-s55`, `engine-n55` |
| Series | `e-series`, `f-series`, `g-series` | |

---

## Metafields

Custom metafields added to Product namespace `custom`:

| Field | Type | Purpose |
|---|---|---|
| `chassis_code` | Single-line text | Displayed on product page |
| `compatible_years` | Single-line text | Displayed on product page |
| `body_styles` | Single-line text | Compatible body styles |
| `installation_note` | Multi-line text | Optional fitting note |

**Path to manage:** `Shopify Admin → Settings → Custom data → Products`

---

## Key Settings Checklist

### Taxes & Duties
- [x] Include VAT in prices: **enabled**
- [x] Belgium VAT rate: **21%**
- [x] Charge tax on shipping: **enabled**
- [x] EU VAT exemption for B2B: **enabled**
- [ ] OSS registration: *(check if €10k EU threshold reached)*

### Payments
- [x] Shopify Payments: *(confirm enabled)*
- [x] Accepted cards: Visa, Mastercard, Amex
- [ ] Bancontact: *(add if not yet enabled — important for Belgian market)*
- [ ] PayPal: *(optional)*

### Checkout
- [x] Guest checkout: enabled
- [x] Company name field: optional (for B2B VAT number)
- [x] EU VAT number field: enabled at checkout
- [ ] Post-purchase upsell: *(consider Reconvert or native Shopify)*

### Email Notifications
- All transactional emails (order confirmation, shipping) customised with Kavoni Design branding
- From address: kavonidesign@gmail.com *(consider a custom domain email for professionalism)*

---

## Shopify Apps

| App | Purpose | Status |
|---|---|---|
| **Klaviyo** | Email marketing integration | ✅ Installed |
| *(add others)* | | |

### Recommended Apps to Consider
| App | Purpose |
|---|---|
| **Reconvert** | Post-purchase upsell |
| **Judge.me** | Product reviews |
| **Tidio / Gorgias** | Live chat / customer support |
| **SEO Manager** | On-page SEO optimisation |
| **Loox** | Photo reviews (UGC) |

---

## Discount Codes

| Code | Type | Value | Notes |
|---|---|---|---|
| `WELCOME10` | Percentage | 10% off | Welcome flow — do not publish publicly |
| `FREESHIP1` | Free shipping | All shipping free | Welcome flow — do not publish publicly |

Create/manage at: `Shopify Admin → Discounts`

---

## Shopify API

| Item | Detail |
|---|---|
| **API version** | *(add current version, e.g. 2024-01)* |
| **Custom apps** | *(list any custom integrations here)* |
| **Webhooks** | *(document any active webhooks — see `integrations.md`)* |
| **Storefront API** | Not currently in use |

---

*Last updated: April 2026*
