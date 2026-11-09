# Island Runner — Thursday Shopping Operations

**Purpose:** Proposed operating workflow for the weekly Powell River shopping service.
**Status:** Planning document; payment collection and order operations are not implemented in the current prototype.

## Decision labels

- **Approved** — Product Owner decision supplied for this workflow.
- **Recommendation** — Suggested operating practice, pending Product Owner approval where it creates a policy.
- **Unresolved** — A decision is needed before the step can become an operating commitment.

## Operating workflow

| When | Status | Step |
|---|---|---|
| Throughout the week | **Approved — OPS-002, OPS-003** | Customers can build carts throughout the week. Scout will initially support approximately 30 commonly purchased product types. |
| Throughout the week | **Approved — OPS-004, OPS-005** | Prices may be verified periodically rather than continuously. Previously verified prices are estimates, not guaranteed purchase prices. |
| When a price is checked | **Recommendation** | Record the retailer/store, product and size, estimated price, and date/time checked. Show a clear “last checked” date/time so customers can judge the estimate's age. This display practice is recommended; no exact freshness threshold has been approved. Do not present unverified prices as confirmed. |
| Wednesday, 6:00 p.m. Pacific Time | **Approved** | Order submission cutoff. Orders must be submitted by this time for consideration in the weekly Thursday run. Handling late submissions and changes to already-submitted orders remains unresolved. |
| After an order is submitted | **Recommendation** | An operator reviews the requested items and quantities, uses the latest verified price information available, and flags uncertain or unverified items. Recheck prices or availability when appropriate; no fixed freshness threshold is approved. Do not change a customer's selections. |
| After review | **Approved — OPS-006** | An operator reviews the order and confirms the final amount with the customer before payment. The customer must approve the final quote before paying. Product prices may still be estimates until the retailer purchase; the quote is not a guarantee of retailer checkout prices. Any optional 5% product-price buffer must be explicitly authorized by the customer and is a spending allowance, not a fee. |
| After the customer receives the quote | **Unresolved** | Define the customer approval method, operator quote turnaround, and response window for that week's run. |
| By Wednesday, 10:00 p.m. Pacific Time | **Approved** | Payment deadline. The customer pays Island Runner by Interac e-Transfer by this time and before purchases are made. Island Runner purchases the selected products from retailers on the customer's behalf. |
| Before purchasing | **Recommendation** | An operator verifies that the expected e-Transfer is received and matches the approved amount. Treat payment as unconfirmed until a human has checked receipt; do not begin purchases based only on a customer's payment notification. |
| Thursday | **Approved — OPS-001, OPS-007** | Island Runner shops in Powell River every Thursday, purchases products on customers' behalf after payment, and coordinates delivery. |
| Thursday, around 6:00 p.m. | **Approved target** | Target home-delivery time across Texada. This is a target, not a guaranteed exact arrival time. Customer notifications, delivery handoff, and what happens if a customer is unavailable remain unresolved. |

## Exceptions and customer choices

### Price changes

- **Approved:** Periodically verified prices are estimates, not guaranteed purchase prices. An operator reviews the order and confirms the final amount with the customer before collecting payment.
- **Approved:** The customer may explicitly authorize an optional 5% product-price buffer. This is a spending allowance, not an additional fee. Unused prepaid funds are refunded.
- **Unresolved:** Define how to proceed if product costs exceed the customer-approved quote and any authorized buffer, and how to handle retailer price changes after quote approval. Do not treat the buffer as permission to charge a fee or an automatic approval for additional spending.

### Missing, unavailable, or mismatched products

- **Approved:** No substitutions are offered. Unavailable items are skipped and refunded. If all products in the order are unavailable, the entire payment, including delivery, is refunded.
- **Unresolved:** Define the operational timing and method for item-level and full-order refunds. Do not replace an unavailable item with a different product.

### Delivery fees and refunds

- **Approved:** The full agreed delivery fee applies when at least one item is delivered. If all products are unavailable, refund the entire payment, including the delivery fee. Unused prepaid funds, including any unused portion of an authorized price buffer, are refunded.
- **Unresolved:** Define the operational timing and method for issuing these refunds and communicating their completion.

### Late orders and unconfirmed payments

- **Approved:** Order submission closes Wednesday at 6:00 p.m. Pacific Time. The customer must pay Island Runner by Interac e-Transfer by Wednesday at 10:00 p.m. Pacific Time and before purchases are made.
- **Unresolved:** Decide whether late submissions or post-submission changes are declined, held for a later Thursday, or accepted when capacity allows. Do not promise same-week fulfillment for late orders before that policy is approved.
- **Recommendation:** Keep orders with unconfirmed payment out of the shopping/purchase list. Notify customers about the approved Wednesday 10:00 p.m. Pacific Time payment deadline using an approved communication method.
- **Unresolved:** Define payment confirmation timing, what happens when payment is short or late, and whether an unpaid order rolls to a later week or is cancelled. Refund handling for unavailable items and fully unavailable orders is approved above; no other late-order cancellation or refund policy is assumed here.

## Potential future automation

These are possibilities for later planning, not approved implementation scope:

- Show a price-check timestamp and flag estimates older than a Product Owner-approved freshness window.
- Collect carts and customer approvals, then prepare an operator order queue and retailer-grouped pick list.
- Calculate a draft quote from available price information and explicitly approved fees or taxes; include a 5% product-price spending allowance only when the customer authorizes it, and do not treat that allowance as a fee.
- Send reminders about the approved cutoff and payment deadline, and quote or price-change reminders, once the reminder channel and message rules are approved.
- Track order states such as submitted, under review, awaiting customer approval, awaiting payment, ready to shop, purchased, and delivered.
- Reconcile e-Transfer notifications against orders, while retaining a human check of actual receipt until a safe and approved process exists.

Automation must not silently change a customer's selections, approve a revised price, treat estimated prices as guaranteed, or mark payment received without reliable confirmation.

## Human approval and control points

Until an explicitly approved process changes these controls, an operator should handle:

- Reviewing each submitted order and checking uncertain product, price, or availability details.
- Obtaining customer approval for the final quote and any changed product selection or total; substitutions are not permitted.
- Confirming e-Transfer receipt before purchase.
- Deciding whether a late order can be accepted once late-order and capacity rules are approved.
- Applying the approved unavailable-item and refund policies, and resolving customer non-response, price increases, short payments, and other exceptions under Product Owner-approved procedures.
- Completing purchases and coordinating delivery; no substitutions or purchases beyond the customer-approved quote and any explicitly authorized spending allowance.

## Outstanding Product Owner decisions

1. Define how the Wednesday 6:00 p.m. Pacific Time cutoff applies to cart edits or changes to an already-submitted order.
2. Define how late submissions are handled and whether there is a weekly capacity limit.
3. Set price-check freshness guidance, the customer-facing timestamp format, and any age threshold for hiding or rechecking estimates.
4. Define quote contents (taxes, service/delivery charges, and other fees), quote validity, customer approval method, and operator turnaround so customers have a reasonable opportunity to meet the Wednesday 10:00 p.m. Pacific Time payment deadline.
5. Define how to proceed if product costs exceed the customer-approved quote and any explicitly authorized 5% spending allowance, and what approval is required before further spending.
6. Define refund timing, method, and customer communication for unavailable items, unused prepaid funds, and fully unavailable orders. Refund amounts are approved as described above.
7. Define how Interac e-Transfer receipt is reconciled and what happens for short, excess, or misidentified payments. The payment deadline is Wednesday at 10:00 p.m. Pacific Time.
8. Define customer notifications, delivery handoff, and failed-delivery handling around the approved target home-delivery time across Texada of Thursday at about 6:00 p.m.; confirm how much timing variation should be communicated.
9. Decide which workflow steps may be automated, what audit trail is needed, and which customer decisions must always remain explicit.

## Scope and implementation note

This document describes the intended service workflow using the supplied Product Owner decisions and clearly marked recommendations. It does not authorize application changes. The current prototype uses demonstration products and prices; live retailer data, checkout, and payment collection remain separate future work requiring discovery and approval. Existing integrations and application code are unchanged.

Once remaining operational questions are resolved and the service policies are approved, they can inform a concise customer-facing FAQ. The FAQ should explain the approved cutoff, payment deadline, quote approval, optional spending allowance, no-substitution and refund rules, full agreed delivery-fee rule, and Thursday delivery target. It should not promise late-order acceptance, a price guarantee, specific refund timing, or an exact delivery arrival time while those procedures remain unresolved.
