# SPIKE-001 — Retail Product Data Feasibility Research

**Project:** Island Runner / Scout
**Research date:** 2026-11-09
**Status:** Discovery only. No integrations or credentials requested.

## Executive summary

The public documentation reviewed does not establish a broadly available, authorized API that can provide Powell River store-specific product assortment, current prices, and availability across the retailers Island Runner needs.

The strongest first step is a direct, written data partnership with one Powell River retailer. Ask for a small, authorized feed or export that identifies the exact store, product/GTIN, package size, price, availability, effective time, and update schedule, plus explicit display and commercial-use rights. This best fits Island Runner's operator-purchase model and gives the retailer a chance to confirm the data matches its checkout and store operations. No public documentation reviewed proves that a particular Powell River retailer will provide such a feed.

In parallel, ask Flipp about a licensed media-partner/NativeX arrangement and local retailer coverage. Flipp documents a route for media properties to display local digital savings experiences, but public materials do not promise a reusable product feed/API, raw data rights, exact Powell River coverage, or freshness/service levels. Treat it as a possible flyer/deal discovery partner, not as a confirmed full-catalog comparison source.

Other findings:

- Walmart Canada publicly promotes an affiliate program through Rakuten, which documents product feeds for approved publishers. Affiliate access is not the same as permission to use Walmart data in Island Runner's operator-purchase flow. Walmart's separate marketplace APIs are seller-facing, and the reviewed Walmart.io restrictions prohibit competitor price/availability analysis absent written permission.
- Canadian Tire has a developer portal with access keys and documentation, but the publicly discoverable material reviewed does not establish a product-price or location-availability API, feed terms, or commercial permission.
- Grocery supplier systems and Instacart retailer catalog tools demonstrate that store-specific price and availability feeds can exist, but their documented access is for participating retailers/suppliers, not an open third-party comparison service.
- GS1 Canada's ECCnet can help normalize Canadian product identity and attributes, but it is not a retail price or store-stock feed.
- VynnAI publicly documents a Canadian grocery-price API with nightly collection, store-level records, a free API tier, and paid plans. Its own methodology describes collection from retailer listings, not a retailer-authorized source relationship. The documentation does not establish rights to redistribute the observations in a customer-facing shopping product. Coverage for Powell River and licensing must be confirmed before considering use.

Until an authorized source, locality, and freshness are verified, Scout should continue to label prototype values as demonstration data and must not present unverified prices or availability as confirmed.

## Source comparison

| Option | Product information | Powell River prices / availability and cadence | Access, permissions, likely cost | Complexity, limitations, reliability |
|---|---|---|---|
| **Flipp — media partnership / NativeX** | Flipp describes local digital savings content, flyers, retailer/brand offers, and native shopping experiences. Public material describes content experiences, not a complete SKU catalog API. | Flipp says its retailer content is local, but no public coverage list for Powell River, store-level in-stock data, exact price freshness, or update SLA was found. Flyer validity dates may help identify offer windows but are not equivalent to live shelf stock. | Media partners (including publishers, apps, and digital properties) can request access to NativeX. A public NativeX agreement describes a limited, non-transferable, non-sublicensable license for the agreed module and a mutually agreed CPM paid to media partners. Pricing and detailed rights depend on an order/contract. Do not assume raw feed or reuse outside the module is permitted. | **Medium/high** if using their provided module; **high/unknown** if Scout needs to ingest and match raw records. Best public partnership route for local flyer discovery. It may not support exact-product matching, live availability, or Island Runner's cart without negotiated rights and technical details. Confirm Powell River retailer coverage and whether a Scout-style search/cart use is allowed. |
| **Walmart Canada affiliate / Walmart APIs** | Walmart Canada affiliate materials document approved product promotion and links. Rakuten's publisher tools can expose advertiser product feeds where available and authorized. Walmart's Marketplace APIs serve sellers managing their own marketplace listings, not general shopping comparisons. | The affiliate page does not promise local store prices/availability or a refresh cadence. Walmart.io documents localized item details and a subscription pickup/delivery collection, but the reviewed terms are not proof this is available for Walmart Canada or Powell River. Walmart Canada Marketplace API material says its Canada APIs were to be decommissioned July 31, 2026; current replacement access and non-seller use require confirmation. | Walmart Canada affiliate approval is via Rakuten. Feed eligibility and the specific advertiser's product-feed access require approval. Affiliate purpose/terms may conflict with Island Runner buying products on behalf of customers rather than referring them to retailer checkout. Walmart.io terms say API use is limited to affiliate advertising and bar use for competitor price/availability analysis without written permission. Fees/commissions and data rights are not fully public in reviewed sources. | **Medium** for approved affiliate links; **high** for custom authorized product access. Strong catalog possibility, but no documented confirmation of Canadian store-level price/stock access. Do not use affiliate/API data for Scout comparison until written terms expressly allow this purpose and data fields. |
| **Canadian Tire** | A developer portal exists with API documentation, access keys, usage reporting, and support. The specific public pages reviewed did not expose a confirmed shopper product search/pricing API. | No documented public guarantee of Powell River store-specific assortment, current price, stock, or refresh cadence was found. | Developer registration/key appears required. Publicly accessible docs did not establish third-party display rights, commercial-use rights, request limits, or fees. Contact Canadian Tire for a partner/data agreement; do not treat portal availability as authorization to compare prices. | **Unknown/high** until endpoints and terms are disclosed. Could be useful if the retailer offers an approved API or feed, but product coverage, locality, SLA, and cost are unanswered. Reliability cannot be assessed from the public portal pages reviewed. |
| **Direct grocery-retailer feed or partnership** | A retailer-provided CSV/API can potentially include GTIN/SKU, name, size, retailer/store, price, promotion, and availability. Instacart's retailer catalog docs show participating retailers can upload item catalogs with store-specific details. GS1 ECCnet provides standardized product attributes shared among trading partners and permitted recipients. | Store-specific price, promotions, and availability are technically supported in retailer systems; Instacart recommends retailers update at least daily and says catalogs update continuously. That is guidance for its retailer storefront, not an offer to Island Runner. The actual cadence and store coverage must be agreed with each retailer. | Requires a direct agreement or participation in the retailer's supplier/commerce program. Loblaw supplier access is for suppliers doing business with Loblaw and confidentiality terms apply; it is not an open shopper API. Costs for a direct retailer feed and ECCnet subscriptions are not public in the sources reviewed; request quotes. | **Medium/high** for one retailer, rising with each different format, contract, and feed. Most aligned with operator purchasing and local reliability if the retailer owns/validates the source. Main limitation is retailer-by-retailer onboarding and no assurance any Powell River chain will participate. |
| **Instacart retailer catalog** | Retailer catalogs can use a universal catalog supplemented with retailer product, price, and location data. | Documentation supports different product details at different store locations and recommends updating at least daily as price/availability changes. | Docs describe retailers onboarding to Instacart, uploading via credentials/SFTP or portal. They do not document a public third-party Scout data license or independent comparison API. Commercial access and cost for Island Runner are unknown. | **Not an open feed option on current evidence.** Useful as evidence of a retailer-partnered model and data fields to request from stores. Availability and reliability depend on retailer uploads and updates. |
| **GS1 Canada ECCnet** | Canadian bilingual product master data, GTIN-linked attributes and content across grocery and general merchandise categories; the registry says it has 700,000+ products and receives ongoing brand-owner updates. | Product attributes may be updated as brand owners submit changes; this is not local retail pricing, promotion, or store inventory. | Subscription and product/trading-partner access controls apply. Data-recipient rights and charges require contacting GS1 Canada. It is an authorized supply-chain data-sharing system, not a public unrestricted catalog. | **Low/medium** as a product identity/attribute aid; cannot provide the needed retailer price comparison by itself. Could reduce matching errors when paired with retailer feeds. Coverage depends on suppliers publishing data and recipient permissions. |
| **Rakuten Advertising / Awin product feeds** | Affiliate networks provide publisher APIs/feeds for participating advertisers' product details and links. Feed fields vary by advertiser. | No guaranteed Powell River store-level price/stock or uniform update interval is documented in the reviewed pages; confirm per feed. | Publisher account, technical access, and often separate advertiser approval are required. Walmart Canada uses Rakuten for its affiliate program; affiliate-use and link attribution terms apply. Awin likewise documents feeds available to publishers and supplied by advertisers. Public setup/pricing details do not establish permission for on-behalf purchasing or a non-affiliate comparison/cart model. | **Medium** for feed plumbing; **high** for ensuring each retailer's feed rights and matching. Could cover online items and links, but local availability and exact intended use may be unsupported. Affiliate model may not fit Island Runner. |
| **VynnAI Canadian grocery pricing API** | Provider documents product names, brands, sizes, categories, shelf/regular/sale prices, retailer/store details, location/date, plus search and product lookup. | Provider says 82 stores across 18 grocery chains, with nightly scheduled collection, and API lookups by province. Its published coverage varies by location and period; methodology explicitly says a price observed at one store does not establish chain-wide pricing and missing dates mean “not observed.” Powell River coverage was not verified. | Provider documents a free plan of 500 API calls/month and paid plans; dataset extracts start at CAD $5,000 for non-commercial research and CAD $15,000 for commercial use, with redistribution priced separately. API terms, source permissions, and commercial customer-facing display rights require direct review. Provider methodology describes prices collected from retailer listings; this report has not independently verified retailer authorization. | **Low/medium** technical API complexity, **high** licensing and data-quality diligence. Nightly observation is not real-time; missing records, product matching, coverage gaps, and source permission remain material risks. Consider only after written confirmation of rights for Island Runner's use and a Powell River coverage sample. |

## Risks and unknowns

1. **Retailer permission and permitted purpose:** Access to product data does not automatically permit redistribution, price comparison, caching, commercial display, or using the data to make purchases on a customer's behalf. Get written terms covering each use.
2. **Local coverage:** No reviewed public source confirms exact Powell River store coverage for Flipp, Walmart, Canadian Tire, or grocery data providers. A provincial or banner-level result is not proof of a local store price.
3. **Price meaning:** Confirm whether a value is regular, sale, loyalty/member, online-only, pickup-only, delivery-only, quantity-limited, or tax-excluded. Island Runner's eventual operator purchase may encounter a different amount at checkout.
4. **Availability:** Product listing or recent price is not an in-stock promise. Agree whether availability is store inventory, online fulfilment eligibility, or merely listed for sale.
5. **Freshness and outages:** Require source timestamp, valid-through time or refresh SLA, feed-health reporting, and a safe fallback. Never silently keep presenting stale prices as current.
6. **Product matching:** UPC/GTIN helps, but equivalent descriptions can differ in size, flavor, pack count, or unit price. Define exact-match rules and never substitute automatically.
7. **Affiliate conflicts:** Affiliate feeds and commission structures usually support referral/advertising workflows. Confirm whether commissions, mandatory click-through, attribution, and retailer checkout are compatible with Island Runner paying retailers on the customer's behalf.
8. **Commercial cost:** Public pages leave most partnership, platform, data, setup, and redistribution fees undisclosed. Get an all-in quote, including minimums, support, usage limits, and cancellation terms.
9. **Scope drift:** A provider that supplies flyers or product metadata may not satisfy the future live-data milestone's need for current, location-specific pricing and availability. Keep flyer discovery and verified purchase data as distinct data classes.

## Recommended first integration approach

Start with a **single-retailer, direct authorized feed pilot**, chosen by the Product Owner from the Powell River retailers Island Runner expects to support first. Ask the retailer for a limited product and store feed or scheduled export, with explicit commercial/customer-facing display permission. Use one store location and a narrow product set before expanding. Require:

- stable item identifiers (GTIN and retailer SKU), exact product name and package size;
- store identifier and product-specific price in CAD, including promotion/loyalty conditions;
- availability definition and timestamp, plus a stated refresh cadence and outage contact;
- permitted use for Island Runner display, comparison, temporary storage/cache, and operator purchasing;
- correction process, data-quality expectations, rate/volume limits, and full costs.

This is a discovery recommendation, not evidence that a retailer has agreed. It is the best fit for local accuracy and Island Runner's intended purchasing model because the retailer can authorize and validate the data directly. In parallel, request Flipp's media-partner materials and ask whether NativeX can cover the intended Powell River flyers and whether its licensed experience supports the Scout flow. Use Flipp only for the uses granted by contract. GS1 ECCnet may be evaluated later to enrich or normalize item metadata, but it cannot replace the retailer price/availability feed.

Do not build against any candidate until the Product Owner selects the pilot retailer and approves its terms, data fields, freshness target, and budget. For any data provider that collects retailer listings itself, require written evidence of its right to license those observations for Island Runner's commercial, customer-facing use.

## Questions requiring Product Owner decisions

1. Which one Powell River retailer and one physical location should anchor the first pilot?
2. Is the first release meant to compare current in-store purchase prices, online/pickup prices, flyer offers, or some explicitly separated subset?
3. What freshness threshold is acceptable, and should each result show a “price checked” timestamp and a warning after a defined age?
4. Should loyalty/member-only prices be excluded unless a customer can use them without creating a retailer account?
5. Is a licensed Flipp flyer module acceptable as an additional discovery experience if it does not provide reusable records for Scout's own comparison/cart?
6. What recurring and one-time data, legal review, and integration budget is available?
7. May a provider's licensed observed prices be considered if it cannot demonstrate direct retailer authorization, or should Island Runner require retailer-originated feeds only?
8. What minimum local product coverage and match confidence must be met before the prototype's demonstration-price label can be replaced with sourced pricing?

## Supporting documentation

### Flipp

- [Flipp FAQ — media partner integration and NativeX](https://corp.flipp.com/faq/)
- [Flipp Platform — retailer and media-partner overview](https://corp.flipp.com/platforms/)
- [Flipp NativeX Terms and Conditions](https://corp.flipp.com/legal-mobile-native-terms-and-conditions/)

### Walmart and affiliate networks

- [Walmart Canada Affiliate Program](https://www.walmart.ca/default/cp/affiliate-program/6000208941216)
- [Walmart I/O terms and conditions](https://walmart.io/termsandcondition)
- [Walmart I/O localized data / third-party access documentation](https://walmart.io/docs/dv-near-real-time/v1/third-party-access/)
- [Walmart Canada Marketplace API getting started](https://developer.walmart.com/ca-marketplace/page/getting-started)
- [Walmart Global APIs webinar PDF — Canada API transition](https://azure-na-assets.contentstack.com/v3/assets/blta7903c6b840b702d/blt4245578865cf1ca2/6a15bb4dc6724fd78f74fff4/Walmart_Global_APIs_Webinar_2026_Canada.pdf?branch=ca_mplearn)
- [Rakuten Advertising product catalog feed guidelines](https://pubhelp.rakutenadvertising.com/hc/en-us/articles/11258487715981-Product-Catalog-Data-Feed-Implementation-Guidelines)
- [Awin Canada FAQ — publisher API and product feeds](https://www.awin.com/ca/faqs)

### Canadian Tire, grocery, and product-data providers

- [Canadian Tire Developer Portal](https://developer.cantire.com/)
- [Canadian Tire interactive documentation](https://developer.cantire.com/interactive-documentation)
- [Instacart retailer catalog documentation](https://docs.instacart.com/storefront/catalog/retailer_catalog)
- [GS1 Canada ECCnet Registry](https://gs1ca.org/new-item-setup/eccnet-registry/)
- [GS1 Canada Content Access](https://www.gs1ca.org/content-access/)
- [Loblaw supplier portal](https://www.loblaw.ca/en/supplier/)
- [Loblaw supplier terms and conditions](https://www.loblaw.ca/en/supplier-terms-and-conditions/)
- [VynnAI API documentation](https://vynn.ai/developers/docs)
- [VynnAI collection methodology](https://vynn.ai/methodology)
- [VynnAI store-level grocery price data](https://vynn.ai/data)
- [VynnAI API pricing and dataset licensing](https://vynn.ai/pricing)

### Verification notes

- Findings above distinguish public documentation from unanswered partner questions. Statements about APIs, feeds, prices, cadence, and costs reflect what the linked pages document as of the research date.
- No account was created, API key requested, paid service purchased, retailer contacted, or endpoint called.
- The Walmart I/O terms page reviewed is dated 2020 and describes an affiliate context; its current application to Walmart Canada must be confirmed directly. The Walmart Canada affiliate page documents affiliate participation, but not a Canada-specific product-price API.
- The Canadian Tire portal could not be inspected beyond publicly indexed portal pages during this review. Its specific product API, local fields, commercial terms, limits, and costs remain unverified.
- Provider claims (including VynnAI's collection size, nightly cadence, and pricing) are self-published and have not been independently audited. Its method page describes collection from retailer listings; this is not proof of retailer authorization or redistribution rights.
- No public webpage inspected establishes that website visibility grants permission for automated collection. This research does not recommend scraping or bypassing any access control.
