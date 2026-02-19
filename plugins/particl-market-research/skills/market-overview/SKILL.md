# Market Overview

Get a high-level view of an e-commerce market or category — top companies, top products, and pricing landscape.

## When to use

When the user wants to understand a market or product category at a high level, not a specific company.

## Workflow

1. **Discover categories** using `get_product_types` (FREE) to find the right `product_type` filter value.
   - Call with no args for root categories, then drill into subcategories with `parent_product_type_id`
   - Use the `product_type_id` from the result as the `product_type` filter in other tools

2. **Get top companies** using `get_market_top_companies`. Costs 1 credit per company returned.
   - Filter by `product_type` to focus on a category
   - Filter by `keyword` for market segments (e.g., 'sustainable', 'luxury')
   - Use `end_date` to analyze a specific point in time

3. **Get top products** using `get_market_top_products`. Costs 1 credit per product returned.
   - Same filters as above for consistent analysis
   - Returns bestselling products across all companies

4. **Get pricing analysis** using `get_market_pricing_analysis`. Costs 1 fixed credit.
   - Same filters for consistency
   - Returns average, median, price range, and distribution buckets

5. **Present findings** with:
   - Market leaders by revenue
   - Bestselling products
   - Pricing landscape (average price, price distribution)
   - Key insights and patterns

## Tips

- Start with `get_product_types` to find the exact category before running market tools
- Use the same `product_type` and `keyword` filters across all calls for consistent data
- `get_market_pricing_analysis` is the cheapest call (1 fixed credit) — good starting point
- The `overall_total_sales_revenue` from `get_market_top_companies` gives market size context
- Compare `end_date` values to see trends over time
