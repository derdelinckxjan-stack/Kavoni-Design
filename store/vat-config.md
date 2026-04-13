# Belgian VAT Configuration — Kavoni Design

> Belgium operates a three-tier VAT system. All Kavoni Design products currently fall under the **21% standard rate**.

---

## VAT Rates at a Glance

| Rate | Category | Applies to Kavoni Design? |
|---|---|---|
| **21%** | Standard rate — most goods & services | ✅ Yes — all current products |
| **12%** | Reduced rate — margarine, certain social housing | ❌ No |
| **6%** | Reduced rate — food, books, pharmaceuticals, renovation | ❌ No |
| **0%** | Zero rate — intra-EU B2B with valid VAT number | ✅ For B2B EU customers |

---

## Our VAT Setup

### Standard Sales (B2C — Belgian & EU Consumers)
- **Rate applied:** 21%
- **Display:** Prices shown **BTW-inclusief** (VAT included) on all product pages
- **Checkout:** VAT amount shown as line item in cart/checkout
- Shopify automatically applies 21% to all orders unless an exemption applies

### B2B EU Sales (Intra-Community Supply)
- If buyer provides a **valid EU VAT number**, supply is **zero-rated** (0% VAT)
- Shopify handles this via the **EU VAT Exemptions** feature
- Buyer must provide VAT number at checkout
- You must retain proof of the VAT number for your records
- Report on **EC Sales List** (Opgave van de intracommunautaire handelingen)

### Export Sales (Outside EU)
- Sales to non-EU countries: **VAT-exempt** (export)
- Shopify: set shipping zone outside EU to 0% tax rate
- Customs duties are the buyer's responsibility (DDP vs DAP — see `shipping.md`)

---

## Shopify VAT Configuration

### Tax Settings Path
`Shopify Admin → Settings → Taxes and duties`

### Key Settings to Verify
- [x] **Charge taxes on shipping rates** — enabled (Belgium requires VAT on shipping)
- [x] **Include tax in prices** — enabled (show BTW-inclusive prices)
- [x] Belgium tax rate: **21%** on all product categories
- [x] EU VAT exemption: enabled for B2B buyers who enter a valid VAT number
- [ ] **OSS (One Stop Shop)** registration — required if EU B2C sales exceed €10,000/year across all EU member states

### OSS Threshold
Belgium participates in the EU **OSS** scheme. If total B2C sales to other EU countries exceed **€10,000/year**, you must either:
1. Register for **OSS** (one registration covers all EU countries), or
2. Register for VAT in each individual EU country

**Current status:** *(update when threshold is approached)*

---

## VAT Invoice Requirements (Belgium)

Every B2B invoice must include:

- [ ] Your full business name and address
- [ ] Your **BTW number** (format: BE 0XXX.XXX.XXX)
- [ ] Customer's full name, address, and VAT number (if B2B)
- [ ] Invoice date and unique sequential invoice number
- [ ] Description of goods/services
- [ ] Net amount (excl. VAT), VAT rate, VAT amount, total incl. VAT
- [ ] Payment terms

### B2C Receipts
For B2C (consumers), a simplified receipt/order confirmation is sufficient — no formal invoice required unless requested.

---

## VAT Return Schedule

| Filing | Frequency | Deadline |
|---|---|---|
| **Monthly** | If annual turnover > €2.5M | 20th of following month |
| **Quarterly** | Most small businesses | 20th of month after quarter end |
| Annual listing | All customers with > €250 purchases | 31 March following year |

**File via:** [intervat.be](https://www.intervat.be) (Belgian tax authority portal)

---

## Important Numbers

| Item | Detail |
|---|---|
| **Standard VAT rate** | 21% |
| **VAT authority** | FOD Financiën / SPF Finances |
| **Portal** | intervat.be |
| **OSS portal** | taxes.be/oss |
| **BTW number** | *(add your BE0XXX.XXX.XXX here)* |

---

## Common Scenarios

**Q: Customer from the Netherlands orders a BMW spoiler. What VAT applies?**
A: If B2C (private individual) — charge 21% Belgian VAT. If B2B with valid NL VAT number — 0% (intra-community supply).

**Q: Customer from the UK orders exhaust tips.**
A: Post-Brexit: UK is outside the EU. Ship VAT-free (export). UK buyer pays UK import duties and VAT on arrival.

**Q: Belgian customer asks for a VAT invoice.**
A: Generate from Shopify (Apps → Invoice generators, or natively). Must include your BTW number and all fields listed above.

---

*Last updated: April 2026 · Always verify current rates at [fiscaliteit.vlaanderen.be](https://www.fiscaliteit.vlaanderen.be)*
