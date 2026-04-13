# Integrations — Kavoni Design

> Third-party tools, webhooks, and data connections for kavonidesign.com.

---

## Integration Stack

| Tool | Category | Status | Connected to |
|---|---|---|---|
| **Klaviyo** | Email marketing | ✅ Active | Shopify |
| **Google Analytics** | Analytics | *(add status)* | Shopify / website |
| **Meta Pixel** | Paid ads tracking | *(add status)* | Shopify |
| **Bpost / DPD** | Shipping carrier | Manual | Shopify fulfilment |
| **Google Search Console** | SEO | *(add status)* | kavonidesign.com |
| *(add others)* | | | |

---

## Klaviyo

### Account Details
| Setting | Value |
|---|---|
| **Plan** | Free tier |
| **Account** | kavonidesign@gmail.com |
| **Shopify integration** | ✅ Connected |
| **Login** | klaviyo.com |

### Active Flows
| Flow | Trigger | Status |
|---|---|---|
| Welcome Series | List subscribe (newsletter form) | ✅ Live |
| Abandoned Cart | Shopify cart abandonment | 📋 To build |
| Post-Purchase | Shopify order placed | 📋 To build |
| Browse Abandonment | Product viewed, no purchase | 📋 Planned |

### Welcome Flow — Technical Config
- **Trigger:** Subscribe to list `[newsletter list name]`
- **Split condition:** Profile property `gift_choice`
  - `= "discount"` → sends `WELCOME10` (10% off)
  - `= "freeship"` → sends `FREESHIP1` (free shipping)
  - *(default / no property)* → sends generic welcome
- **Discount codes managed in:** Shopify Admin → Discounts
- **Codes used:** `WELCOME10` · `FREESHIP1`

### Klaviyo Segments (Planned)
| Segment | Condition |
|---|---|
| M3 owners | Shopify tag contains `model-m3` OR profile property `bmw_model` = M3 |
| M4 owners | Tag / property = M4 |
| Recent buyers (90d) | Placed order in last 90 days |
| VIP customers | Placed 3+ orders |
| Unengaged (180d) | No email open in 180 days |

### Key Metrics to Monitor (Klaviyo dashboard)
- Welcome flow open rate (target: >40%)
- Welcome flow click rate (target: >5%)
- Revenue attributed to flows (monthly)
- List growth rate (weekly)

---

## Shopify → Klaviyo Data Sync

| Shopify event | Klaviyo event/property |
|---|---|
| Customer created | Profile created + email subscribed |
| Order placed | `Placed Order` event |
| Order fulfilled | `Fulfilled Order` event |
| Order cancelled | `Cancelled Order` event |
| Cart abandoned | `Started Checkout` event |
| Product viewed | `Viewed Product` event *(requires Klaviyo JS snippet)* |
| Subscribe via form | `Subscribed to List` + custom `gift_choice` property |

Ensure the **Klaviyo script** is installed in the Shopify theme `<head>` for full event tracking.

---

## Email Signup Form

### Form Config
- **Platform:** Klaviyo embedded form
- **Location:** Website footer + optional pop-up
- **Incentive:** Mystery gift — customer chooses 10% off or free shipping
- **Custom property captured:** `gift_choice` (`"discount"` or `"freeship"`)
- **List added to:** *(add Klaviyo list name)*

### Form HTML
See `faq-shopify-paste.html` in the workspace folder for the sign-up widget HTML/CSS.

---

## Google Analytics / GA4

| Setting | Value |
|---|---|
| **Property** | *(add GA4 property ID)* |
| **Connected via** | Shopify Google channel or manual GTM |
| **Key goals tracked** | Purchase, Add to cart, Begin checkout |
| **Enhanced e-commerce** | *(confirm enabled)* |

---

## Meta (Facebook) Pixel

| Setting | Value |
|---|---|
| **Pixel ID** | *(add pixel ID)* |
| **Connected via** | Shopify Facebook channel |
| **Events tracked** | ViewContent, AddToCart, Purchase |
| **Catalogue sync** | *(confirm if product catalogue synced for Dynamic Ads)* |

---

## Webhooks (Active)

Document any active Shopify webhooks here:

| Event | Endpoint | Purpose |
|---|---|---|
| *(add)* | *(URL)* | *(description)* |

---

## Domains & DNS

| Domain | Registrar | Status |
|---|---|---|
| kavonidesign.com | *(add registrar)* | ✅ Active — points to Shopify |
| *(www redirect)* | | |

DNS managed via registrar. Shopify provides SSL automatically.

---

## Credentials & Access

> ⚠️ Do not store passwords here. Use a password manager (e.g. 1Password / Bitwarden).

| Service | Login email | Notes |
|---|---|---|
| Shopify | kavonidesign@gmail.com | Owner account |
| Klaviyo | kavonidesign@gmail.com | Free plan |
| Google Analytics | *(add)* | |
| Meta Business | *(add)* | |
| Domain registrar | *(add)* | |

---

## Future Integrations to Consider

| Tool | Purpose | Priority |
|---|---|---|
| **Judge.me / Loox** | Product reviews with photos | High |
| **Gorgias** | Helpdesk integrated with Shopify | Medium |
| **Google Merchant Centre** | Google Shopping ads | High |
| **TikTok Pixel** | TikTok ad tracking | Low |
| **Returnly / Loop** | Returns management portal | Medium |
| **Sufio / Invoicify** | Automated VAT invoice generation | High (B2B) |

---

*Last updated: April 2026*
