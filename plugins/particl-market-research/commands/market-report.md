# /particl:market-report

Generate a comprehensive market report for a product category or market segment.

## Arguments

- `category` (required): The product category or market segment to analyze (e.g., "athleisure", "sustainable fashion", "wireless earbuds")

## Steps

1. Call `get_credit_balance` to verify sufficient credits (~50 needed)
2. Call `get_market_top_companies` with `keyword` set to the category
3. Call `get_market_top_products` with the same `keyword` filter
4. Call `get_market_pricing_analysis` with the same `keyword` filter
5. Compile results into a structured report:
   - Market size and top players
   - Bestselling products
   - Pricing landscape (average, median, distribution)
   - Key insights and opportunities
