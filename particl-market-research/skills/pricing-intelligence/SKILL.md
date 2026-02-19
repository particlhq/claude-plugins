# Pricing Intelligence

Analyze pricing strategies across a market or for a specific company's product catalog.

## When to use

When the user asks about pricing — market averages, price distribution, a company's pricing tiers, or price comparisons.

## Workflow

1. **Get market pricing analysis** using `get_market_pricing_analysis`. Costs 1 fixed credit.
   - Filter by `product_type` and/or `keyword` to focus on a segment
   - Returns summary (average, median, min, max) and price distribution buckets

2. **Compare specific companies** using `get_company_products` for each company. Costs 1 credit per product.
   - Sort by `price` with `sort_direction: "desc"` for premium products
   - Sort by `price` with `sort_direction: "asc"` for entry-level products
   - Use `min_price` and `max_price` to explore specific tiers

3. **Present findings** with:
   - Market-wide pricing summary
   - Price distribution (where most products are priced)
   - Company-level pricing compared to market averages
   - Positioning insights (premium vs. value)

## Tips

- Start with `get_market_pricing_analysis` — it's the cheapest way to understand pricing
- Use `min_price` and `max_price` on `get_company_products` to count products in price tiers
- Compare `avg_current_price` vs `avg_full_price` on products to find discounting patterns
