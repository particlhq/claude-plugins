# Competitor Analysis

Analyze a company's e-commerce presence, product catalog, marketing activity, and sales performance using Particl data.

## When to use

When the user wants to research a specific company or brand — their products, pricing, bestsellers, marketing strategy, or overall performance.

## Workflow

1. **Find the company** using `search_companies` with the company name or domain. This is FREE.
   - Extract the `company_id` from the results

2. **Get company details** using `get_company_details` with the `company_id`. Costs 1 credit.
   - Shows company profile: name, domain, country, vertical, product count, top categories
   - Check `has_product_data` — if false, skip product tools (no data available)

3. **Discover categories** using `get_product_types` (FREE) to find valid `product_type` filter values.
   - Call with no args for root categories, then drill into subcategories with `parent_product_type_id`

4. **Analyze their product catalog** using `get_company_products` with the `company_id`. Costs 1 credit per product returned.
   - Default sort is by `sales_revenue` descending (bestsellers first)
   - Use `page_size` to control how many products (default 25, max 100)
   - Use `product_type` or `keyword` filters to narrow by category
   - Use `title_search` to search by product name (e.g., 'tank top', 'winter jacket')
   - Use `start_date` and `end_date` to control the sales data window
   - Paginate with `page` parameter for deeper exploration

5. **Review their marketing** using `get_company_marketing_assets` for emails, social posts, and ads. Costs 1 credit/row.
   - Filter by `asset_types`: 'email', 'instagram_post', 'facebook_ads', 'sms', 'homepage_screenshot'
   - Use `get_company_marketing_stats` for aggregated engagement metrics (1 credit)

6. **Check promotional events** using `get_company_events` for launches, sales, restocks. Costs 1 credit/row.

7. **Present findings** with:
   - Company overview (vertical, product count, top categories)
   - Top products by revenue
   - Price range analysis
   - Marketing activity and engagement
   - Notable patterns (new launches, discounting, promotional events)

## Tips

- Always check credits first with `get_credit_balance` if doing a large analysis
- Start with a small `page_size` (10-15) to get an overview before going deeper
- Use `sort_by: "launch_date"` with `sort_direction: "desc"` to find newest products
- Use `sort_by: "price"` to understand pricing tiers
- Use `title_search` instead of `keyword` when searching for product names
