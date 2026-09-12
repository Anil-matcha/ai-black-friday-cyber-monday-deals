# Deal data

`deals.csv` is the canonical machine-readable list. Keep one product offer per row and do not add fake or placeholder deals.

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

## Rules

- Use ISO-8601 timestamps, for example `2026-11-27T00:00:00Z`.
- Keep prices and currencies explicit, for example `USD 99/year`.
- Do not calculate a discount when the vendor only states “up to” without plan-level pricing.
- Mark an offer `expired` after its end date; do not silently delete it.
- Keep watching and historical rows out of the active README table.
