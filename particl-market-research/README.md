# Particl Market Research Plugin

E-commerce market research, competitor intelligence, and marketing analytics for Claude.

## What it does

This plugin connects Claude to [Particl's](https://particl.com) market research platform, giving you access to sales estimates, pricing data, product catalogs, and marketing intelligence across thousands of e-commerce brands.

## Tools available

| Tool | Cost | Description |
|------|------|-------------|
| `search_companies` | FREE | Search for companies by name or domain |
| `get_product_types` | FREE | Browse product type taxonomy for category filtering |
| `get_company_details` | 1 credit | Get company profile with product counts and top categories |
| `get_company_products` | 1 credit/row | Browse a company's product catalog with full filtering and sorting |
| `get_market_top_products` | 1 credit/row | Bestselling products in a market |
| `get_market_top_companies` | 1 credit/row | Top companies in a market |
| `get_market_pricing_analysis` | 1 credit | Pricing summary for a market |
| `search_market_products` | 1 credit/row | Search products across all companies |
| `get_company_marketing_assets` | 1 credit/row | Emails, Instagram posts, Facebook ads, SMS, screenshots |
| `get_company_marketing_stats` | 1 credit | Aggregated engagement stats and posting patterns |
| `get_marketing_asset_details` | 1 credit | Full details of a specific marketing asset |
| `get_company_events` | 1 credit/row | Product launches, sales, restocks, price changes |
| `get_credit_balance` | FREE | Check your remaining credits |

## Getting started

1. Install this plugin in Claude
2. You'll be prompted to sign in with your Particl account (OAuth)
3. Ask Claude to research any e-commerce market or company

## Example prompts

- "What are the top-selling athletic wear brands right now?"
- "Compare Lululemon and Alo Yoga's product catalogs"
- "What's the average price point in the sustainable fashion market?"
- "Show me Nike's recent marketing emails and Instagram posts"
- "What promotional events has Glossier run in the last month?"
- "How many credits do I have left?"

## Authentication

This plugin uses OAuth to connect to your Particl account. Your existing export credits are used for MCP queries (1 credit per data row for most tools, some tools are free).
