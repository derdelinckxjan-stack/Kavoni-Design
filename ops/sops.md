# Standard Operating Procedures — Kavoni Design

> Step-by-step processes for running kavonidesign.com consistently and efficiently.

---

## SOP 001 — New Order Processing

**Trigger:** New order notification received (Shopify email / app push)

1. **Verify payment** — confirm order is paid (not pending) in Shopify Admin
2. **Check inventory** — confirm item is in stock
   - If in stock → proceed to step 3
   - If out of stock → go to SOP 004 (Out of Stock Order)
3. **Check shipping details** — verify address is complete and legible
4. **Print/prepare packing slip** — generate from Shopify
5. **Pack the order** — use appropriate packaging (see `shipping.md`)
6. **Photograph parcel** before sealing (for dispute protection)
7. **Book carrier** — Bpost/DPD/UPS depending on zone
8. **Add tracking number** to Shopify order
9. **Mark as fulfilled** in Shopify → auto-sends tracking email to customer
10. **File packing slip** (digital or physical)

**Target time:** Same day if order placed before 13:00 CET

---

## SOP 002 — New Product Listing

**Trigger:** New product sourced and ready to list

1. **Gather product info:** name, chassis fitment, year range, specs, supplier SKU
2. **Take/request product photos** (min. 3: front, detail, lifestyle/fitment)
3. **Write product description** using template in `marketing/copy-bank.md`
4. **Set pricing:** calculate from cost price + margin target, round to €XX9 or €XX5, ensure VAT-inclusive
5. **Create Shopify listing:**
   - Title: `[Type] — [Model] [Chassis] — [Spec/Finish]`
   - Add to correct collection(s) — by model and by category
   - Set product type, vendor, tags (model, chassis, category)
   - Add metafield: chassis code, compatible years
   - Enter weight for shipping
   - Assign SKU
6. **Set inventory** — enable tracking, enter quantity
7. **Preview on storefront** — check mobile and desktop
8. **Publish** — set to Active
9. **Add to relevant `models/` markdown** if new model coverage

---

## SOP 003 — Customer Inquiry Response

**Trigger:** Email or contact form inquiry received

**Target response time:** Within 24 hours on business days

1. **Read inquiry fully** before replying
2. **Identify type:** fitment question / order status / return request / general
3. **Check relevant info:** Shopify order history, product page, `customer-service.md` FAQ
4. **Draft reply** using tone guide: professional, warm, precise (see `ops/customer-service.md`)
5. **If fitment question:** verify against `models/` documentation before confirming compatibility
6. **Send reply** from kavonidesign@gmail.com
7. **Flag if unresolved** — follow up within 48 hours if waiting on supplier info

---

## SOP 004 — Out of Stock Order

**Trigger:** Order placed for an item with no stock

1. **Do not fulfil yet** — hold the order
2. **Email customer within 24 hours** — inform of delay, give estimated restock date
3. **Contact supplier** for lead time (see `ops/suppliers.md`)
4. **Update customer** when order ships
5. **If lead time > 14 days:** offer customer choice of wait or full refund
6. **Mark product as "Available on order"** in Shopify if this is a recurring situation

---

## SOP 005 — Return / Refund Processing

**Trigger:** Customer requests return (see full policy in `ops/customer-service.md`)

1. **Receive return request** — verify within 30-day window
2. **Confirm reason:** defective / wrong item / change of mind
3. **If defective or wrong item:**
   - Apologise and arrange free return shipping label
   - Once received and inspected, issue full refund or replacement
4. **If change of mind:**
   - Customer arranges and pays return shipping
   - Item must be unused, in original packaging
   - Refund product value only (not original shipping) once received
5. **Process refund in Shopify** → Admin → Orders → Refund
6. **Restock item** if in resaleable condition
7. **Log return reason** in a simple spreadsheet for trend monitoring

---

## SOP 006 — Weekly Store Review

**Frequency:** Every Monday morning (~30 minutes)

1. **Check orders** — any outstanding, unfulfilled, or flagged orders?
2. **Check messages/emails** — any unanswered inquiries?
3. **Review Shopify analytics:**
   - Sessions, conversion rate, top products
   - Any abandoned checkouts worth recovering?
4. **Check inventory levels** — any items running low (< 3 units)?
5. **Review Klaviyo** — check email flow health, open rates, any bounces
6. **Check supplier lead times** for any pending restocks
7. **Update `ops/sops.md`** if any process needs adjustment

---

## SOP 007 — Product Restock

**Trigger:** Inventory drops below reorder threshold (default: 3 units)

1. **Identify item** — SKU, supplier, last order quantity
2. **Contact supplier** — email or portal order (see `ops/suppliers.md`)
3. **Log expected delivery date** in Shopify or a note on the product
4. **On arrival:**
   - Inspect items — check for transit damage
   - Photograph stock
   - Update Shopify inventory count
5. **If item was out of stock during reorder period:** notify any waiting customers

---

*Last updated: April 2026*
