# Deal data

`deals.csv` is the canonical machine-readable list of confirmed offers. Keep one product offer per row and do not add fake or placeholder deals.

`watchlist.csv` contains 2026 leads discovered from deal directories and research pages. Watchlist rows are intentionally not confirmed and must not be presented as active discounts.

## Fields

| Field | Meaning |
| --- | --- |
| `year` | Sale year, currently `2026` |
| `product` | Product name |
| `company` | Vendor or company name |
| `category` | One of the categories in the root README |
| `use_case` | Short buyer-focused description |
| `official_url` | Official product or offer URL |
| `pricing_url` | Official pricing or checkout URL |
| `regular_price` | Normal price before the promotion |
| `sale_price` | Promotional price |
| `discount_percent` | Numeric percentage, without the `%` sign |
| `deal_type` | `annual`, `monthly`, `lifetime`, `credits`, or `bundle` |
| `coupon_code` | Code, or `NO_CODE` when automatically applied |
| `start_date_utc` | ISO-8601 UTC start timestamp |
| `end_date_utc` | ISO-8601 UTC end timestamp |
| `eligibility` | New-user, existing-user, regional, or other restrictions |
| `renewal_terms` | What happens after the promotional period |
| `verified_at_utc` | Last time the terms were checked |
| `status` | `confirmed`, `watching`, `expired`, or `rejected` |
| `notes` | Important caveats or verification context |

## Watchlist fields

| Field | Meaning |
| --- | --- |
| `year` | Sale year, currently `2026` |
| `product` | Product name |
| `company` | Vendor name when known |
| `category` | Buyer-facing category |
| `lead_status` | `watching`, `no_offer_spotted`, `expected_from_history`, `listed_on_2026_page`, or `marketplace_lead` |
| `deal_signal` | Short summary of what the source claims or suggests |
| `official_url` | Official product URL, not a coupon or affiliate redirect |
| `discovered_from` | Third-party page where the lead was found |
| `source_checked_at_utc` | ISO-8601 date or UTC timestamp when the lead page was checked |
| `notes` | Why the lead still needs verification |

## Rules

- Use ISO-8601 timestamps, for example `2026-11-27T00:00:00Z`.
- Keep prices and currencies explicit, for example `USD 99/year`.
- Do not calculate a discount when the vendor only states “up to” without plan-level pricing.
- Mark an offer `expired` after its end date; do not silently delete it.
- Keep watching and historical rows out of the active README table.
- Never copy a third-party coupon into `deals.csv` without checking the vendor's own offer or checkout page.
