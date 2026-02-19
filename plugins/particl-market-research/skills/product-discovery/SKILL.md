# Product Discovery

Search and discover products across the entire e-commerce market or within a specific company.

## When to use

When the user wants to find specific products, explore what's selling, discover new launches, or browse a catalog.

## Workflow

### Market-wide search
Use `search_market_products` to search across ALL tracked companies. Costs 1 credit per product.
- `keyword`: search by product keywords (e.g., 'recycled', 'wireless')
- `product_type`: filter by category
- `brand`: filter by brand name
- `min_price` / `max_price`: price range filters
- `sort_by`: `sales_revenue` (default), `sales_volume`, `price`, or `launch_date`
- `sort_direction`: `desc` (default) or `asc`
- `start_date` / `end_date`: control the sales data window

### Company-specific search
Use `get_company_products` with a `company_id` for the same capabilities scoped to one company.
- Find the `company_id` first with `search_companies` (FREE)
- Same filters and sorting as market-wide search

### Pagination
Both tools support pagination:
- `page_size`: 1-100 (default 25)
- `page`: 0-indexed page number
- Response includes `has_more` and `total_count` for navigation

## Tips

- Use `sort_by: "launch_date"` with `sort_direction: "desc"` for newest products
- Use `sort_by: "sales_revenue"` for bestsellers
- Combine `keyword` with `product_type` for precise filtering
- Check `has_more` in the response to know if there are additional pages
