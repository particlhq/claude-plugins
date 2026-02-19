# Market Overview

Get a high-level view of an e-commerce market or category — top companies, top products, and pricing landscape.

## When to use

When the user wants to understand a market or product category at a high level, not a specific company.

## Workflow

1. **Get top companies** using `get_market_top_companies`. Costs 1 credit per company returned.
   - Filter by `product_type` to focus on a category (e.g., filter by a product type ID)
   - Filter by `keyword` for market segments (e.g., 'sustainable', 'luxury')
   - Use `end_date` to analyze a specific point in time

2. **Get top products** using `get_market_top_products`. Costs 1 credit per product returned.
   - Same filters as above for consistent analysis
   - Returns bestselling products across all companies

3. **Get pricing analysis** using `get_market_pricing_analysis`. Costs 1 fixed credit.
   - Same filters for consistency
   - Returns average, median, price range, and distribution buckets

4. **Present findings** with:
   - Market leaders by revenue
   - Bestselling products
   - Pricing landscape (average price, price distribution)
   - Key insights and patterns

## Tips

- Use the same `product_type` and `keyword` filters across all three calls for consistent data
- `get_market_pricing_analysis` is the cheapest call (1 fixed credit) — good starting point
- The `overall_total_sales_revenue` from `get_market_top_companies` gives market size context
- Compare `end_date` values to see trends over time
