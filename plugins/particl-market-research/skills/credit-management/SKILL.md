# Credit Management

Understand and manage Particl API credit usage.

## When to use

When the user asks about credits, wants to check their balance, or needs to plan a research task within their credit budget.

## Workflow

1. **Check balance** using `get_credit_balance`. FREE.
   - Returns `credit_limit`, `credits_used`, and `credits_remaining`

2. **Estimate costs** before running queries:
   - `search_companies`: FREE
   - `get_credit_balance`: FREE
   - `get_company_details`: 1 credit
   - `get_market_pricing_analysis`: 1 credit (fixed)
   - `get_market_top_products`: 1 credit per product returned
   - `get_market_top_companies`: 1 credit per company returned
   - `search_market_products`: 1 credit per product returned
   - `get_company_products`: 1 credit per product returned

3. **Optimize usage**:
   - Use smaller `page_size` values to limit credit consumption
   - Start with the cheapest tools: `search_companies` (free) and `get_market_pricing_analysis` (1 credit)
   - Use filters to narrow results before fetching large datasets

## Cost estimation examples

| Task | Estimated credits |
|------|-------------------|
| Company lookup + top 10 products | ~11 credits |
| Market overview (top companies + products + pricing) | ~51 credits |
| Quick pricing check for a category | 1 credit |
| Full competitor analysis (details + 50 products) | ~51 credits |
