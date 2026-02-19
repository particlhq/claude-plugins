# Credit Management

Understand and manage Particl API credit usage.

## When to use

When the user asks about credits, wants to check their balance, or needs to plan a research task within their credit budget.

## Workflow

1. **Check balance** using `get_credit_balance`. FREE.
   - Returns `credit_limit`, `credits_used`, and `credits_remaining`

2. **Estimate costs** before running queries:
   - `search_companies`: FREE
   - `get_product_types`: FREE
   - `get_credit_balance`: FREE
   - `get_company_details`: 1 credit
   - `get_market_pricing_analysis`: 1 credit (fixed)
   - `get_company_marketing_stats`: 1 credit (fixed)
   - `get_marketing_asset_details`: 1 credit (fixed)
   - `get_market_top_products`: 1 credit per product returned
   - `get_market_top_companies`: 1 credit per company returned
   - `search_market_products`: 1 credit per product returned
   - `get_company_products`: 1 credit per product returned
   - `get_company_marketing_assets`: 1 credit per asset returned
   - `get_company_events`: 1 credit per event returned

3. **Optimize usage**:
   - Use smaller `page_size` values to limit credit consumption
   - Start with FREE tools: `search_companies`, `get_product_types`
   - Then use cheap fixed-cost tools: `get_market_pricing_analysis`, `get_company_marketing_stats` (1 credit each)
   - Use filters to narrow results before fetching large datasets

## Cost estimation examples

| Task | Estimated credits |
|------|-------------------|
| Company lookup + top 10 products | ~11 credits |
| Market overview (top companies + products + pricing) | ~51 credits |
| Quick pricing check for a category | 1 credit |
| Full competitor analysis (details + 50 products + marketing stats) | ~53 credits |
| Marketing deep-dive (stats + 25 assets + 25 events) | ~51 credits |
