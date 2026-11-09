# Product Backlog

## Approved: Iteration 3.3A - Scout Shopping Experience Prototype

**Goal:** Validate a simple, accessible shopping experience within Island Runner, without requiring customers to leave the site to search demonstration products.

### Scope

- Search a small demonstration product catalogue.
- Display up to three relevant product options per search.
- Show each option's product name, size, retailer, and clearly labelled demonstration price.
- Let customers choose which products to add to their cart; never automatically select or substitute products.
- Support multiple products from different retailers.
- Let customers adjust quantities and remove products.
- Calculate the running product subtotal as the sum of each item's price multiplied by its quantity.
- Let customers review the cart grouped by retailer.

### UX requirements

- Keep Scout as the primary shopping experience.
- Minimize cognitive load.
- Use progressive disclosure.
- Never automatically select or substitute products.
- Prioritize mobile accessibility.

### Acceptance criteria

1. Customers can search the demonstration catalogue without leaving Island Runner.
2. Scout displays no more than three options per search.
3. Customers can add their chosen products to a cart.
4. Quantity changes and product removals update the subtotal correctly.
5. Cart review clearly identifies products and retailers, grouped by retailer.
6. All demonstration prices are explicitly labelled as demonstration prices.
7. The existing Google Forms integration is preserved and unchanged.
8. The experience is tested on desktop and mobile where practical; report any platform that could not be tested.

## Approved ticket: IR-FAQ-001 - Customer Frequently Asked Questions

Add a simple, accessible FAQ near the bottom of the homepage using native HTML `details`/`summary` controls. Answers remain collapsed until a customer opens a question, and the FAQ stays visually secondary to Scout.

### Approved content

Include these questions and answer them using approved operational policies:

1. How does Island Runner work?
2. When do you shop?
3. When is the order deadline?
4. How and when do I pay?
5. When will my shopping arrive?
6. Where do you deliver?
7. What happens if something is unavailable?
8. Do you offer substitutions?
9. What happens if prices change?
10. What happens if only part of my order is available?
11. Are Scout's prices guaranteed?

State that Island Runner shops in Powell River every Thursday; orders close Wednesday at 6 p.m. Pacific; customers approve the final quote before paying by e-Transfer by Wednesday at 10 p.m. Pacific; and Thursday home delivery across Texada targets around 6 p.m. State that substitutions are not offered and unavailable items are skipped and refunded. Describe the optional, customer-authorized 5% product-price buffer, refunds of unused prepaid funds, the full agreed delivery fee when at least one item is delivered, and the full refund including delivery when the entire order is unavailable. Clearly say Scout's current product prices are demonstrations, not verified live prices.

The FAQ must also clearly state that the current prototype does not accept real customer orders or payments. This ticket adds explanatory content only; it does not implement booking, checkout, or payment features.

### Acceptance criteria

1. The homepage displays the heading **"Questions? Scout's got answers! 🦊"** near the bottom, visually secondary to Scout.
2. All eleven approved questions appear as native `details`/`summary` items, collapsed by default and operable by keyboard and pointer.
3. Answers are concise, friendly, mobile-friendly, and match the approved weekly schedule, quote/payment, delivery, unavailable-item, refund, buffer, and demonstration-price policies.
4. The FAQ does not imply that the prototype accepts real orders or payments.
5. The FAQ does not show delivery forms or checkout controls or repeat the FAQ elsewhere on the homepage.
6. Existing Scout search/cart behavior and Google Forms code/integrations remain unchanged.
7. No dependencies, booking features, or payment features are added.

## Future milestone: Iteration 3.3B - Live Product Data

This is a separate future milestone requiring discovery and Product Owner approval. Do not implement live data integration as part of Iteration 3.3A.

### Discovery scope

- Identify reliable sources for retailer product information.
- Investigate current price and availability data.
- Investigate product matching and comparison across retailers.
- Document data-source permissions, limitations, and reliability.

## Future work (separate scope)

The following require separate planning and approval:

- Checkout improvements.
- Payment processing.
- Optional store consolidation. Any store-consolidation suggestions must remain optional.
