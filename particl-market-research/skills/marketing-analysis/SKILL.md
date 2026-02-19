# Marketing Analysis

Analyze a company's marketing strategy — emails, social media, ads, and promotional events.

## When to use

When the user wants to understand a company's marketing activity, email campaigns, social media engagement, ad creatives, or promotional calendar.

## Workflow

1. **Find the company** using `search_companies` with the company name or domain. This is FREE.
   - Extract the `company_id` from the results

2. **Get marketing stats** using `get_company_marketing_stats`. Costs 1 credit.
   - Returns total assets by type, engagement metrics, posting frequency, best posting hours
   - Good starting point for understanding the company's marketing profile

3. **Browse marketing assets** using `get_company_marketing_assets`. Costs 1 credit per asset.
   - Filter by `asset_types` to focus:
     - `'email'` — marketing emails with subject lines and content
     - `'instagram_post'` — Instagram posts with likes, comments, views
     - `'facebook_ads'` — Meta/Facebook ads with creative cards and targeting
     - `'sms'` — SMS/text message campaigns
     - `'homepage_screenshot'` — website homepage screenshots showing promotions
   - Use `start_date` / `end_date` to focus on a time period
   - Paginate with `page` and `page_size`

4. **Get asset details** using `get_marketing_asset_details` for full content of a specific asset. Costs 1 credit.

5. **Check promotional events** using `get_company_events`. Costs 1 credit per event.
   - Filter by `event_types`:
     - `'sitewide_discount'` — sales and promotions
     - `'major_product_launch'` — new product launches
     - `'major_restock'` — restocks
     - `'category_launch'` / `'category_discontinued'` — category changes
     - `'major_price_decrease'` / `'major_price_increase'` — pricing shifts
     - `'product_highlight'` — featured products
   - Filter by `channels` to see which marketing channels promoted each event

6. **Present findings** with:
   - Marketing channel mix (email vs social vs ads)
   - Posting frequency and best times
   - Engagement metrics (likes, comments, shares)
   - Recent campaigns and themes
   - Promotional event calendar
   - Content strategy patterns

## Tips

- Start with `get_company_marketing_stats` (1 credit) for the big picture
- Use `asset_types` filter to focus on one channel at a time
- Compare posting frequency across channels to understand marketing strategy
- Use `get_company_events` to correlate marketing pushes with business events
