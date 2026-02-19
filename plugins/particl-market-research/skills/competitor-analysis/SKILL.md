# Competitor Analysis

Analyze a company's e-commerce presence, product catalog, and sales performance using Particl data.

## When to use

When the user wants to research a specific company or brand — their products, pricing, bestsellers, or overall performance.

## Workflow

1. **Find the company** using `search_companies` with the company name or domain. This is FREE.
   - Extract the `company_id` from the results (e.g., `lululemon-com`)

2. **Get company details** using `get_company_details` with the `company_id`. Costs 1 credit.
   - Shows company profile: name, domain, country, start date

3. **Analyze their product catalog** using `get_company_products` with the `company_id`. Costs 1 credit per product returned.
   - Default sort is by `sales_revenue` descending (bestsellers first)
   - Use `page_size` to control how many products (default 25, max 100)
   - Use `product_type` or `keyword` filters to narrow by category
   - Use `start_date` and `end_date` to control the sales data window
   - Paginate with `page` parameter for deeper exploration

4. **Present findings** with:
   - Company overview
   - Top products by revenue
   - Price range analysis
   - Notable patterns (new launches, discounting, category focus)

## Tips

- Always check credits first with `get_credit_balance` if doing a large analysis
- Start with a small `page_size` (10-15) to get an overview before going deeper
- Use `sort_by: "launch_date"` with `sort_direction: "desc"` to find newest products
- Use `sort_by: "price"` to understand pricing tiers
