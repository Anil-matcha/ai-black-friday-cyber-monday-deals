# Contributing

Thanks for helping keep the list useful and trustworthy.

## Before opening a pull request

Confirm that your entry has:

1. An official product or pricing URL.
2. The regular price and promotional price in the same currency.
3. A working coupon code, or confirmation that checkout applies the discount automatically.
4. Start and end dates, including the timezone where possible.
5. Eligibility and renewal details.
6. A source that a reviewer can check without signing in or using an affiliate redirect.

Predicted discounts, unverified coupon codes, and offers copied only from another directory will not be accepted as confirmed deals.

## Pull request format

Add one row to [`data/deals.csv`](data/deals.csv), then include a short summary in your pull request:

```text
Product:
Category:
Offer:
Official source:
Dates and timezone:
Eligibility:
Renewal terms:
Last verified:
```

Use `status=confirmed` only when the offer is live or the vendor has published the exact terms. Use `status=watching` for a product with no confirmed 2026 offer; watching rows do not belong in the active deal table.

## Review standards

Maintainers may edit formatting, request evidence, move an entry to another category, or mark an offer expired when its end date passes. We prioritize accuracy over the number of listings.

We do not accept:

- Spam, malware, deceptive products, or misleading pricing
- Duplicate submissions
- Unclear “up to” discounts without a qualifying plan or price
- Offers without dates or source links
- Affiliate links that obscure the official destination

## Code of conduct

Be concise, respectful, and transparent about commercial relationships. Disagreements are welcome; personal attacks and manipulation of the list are not.
