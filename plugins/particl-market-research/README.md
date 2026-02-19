# Particl Market Research Plugin

E-commerce market research and competitor intelligence for Claude.

## What it does

This plugin connects Claude to [Particl's](https://particl.com) market research platform, giving you access to sales estimates, pricing data, and product catalogs across thousands of e-commerce brands.

## Tools available

| Tool | Cost | Description |
|------|------|-------------|
| `search_companies` | FREE | Search for companies by name or domain |
| `get_company_details` | 1 credit | Get company profile info |
| `get_company_products` | 1 credit/row | Browse a company's product catalog with full filtering and sorting |
| `get_market_top_products` | 1 credit/row | Bestselling products in a market |
| `get_market_top_companies` | 1 credit/row | Top companies in a market |
| `get_market_pricing_analysis` | 1 credit | Pricing summary for a market |
| `search_market_products` | 1 credit/row | Search products across all companies |
| `get_credit_balance` | FREE | Check your remaining credits |

## Getting started

1. Install this plugin in Claude
2. You'll be prompted to sign in with your Particl account (OAuth)
3. Ask Claude to research any e-commerce market or company

## Example prompts

- "What are the top-selling athletic wear brands right now?"
- "Compare Lululemon and Alo Yoga's product catalogs"
- "What's the average price point in the sustainable fashion market?"
- "Show me the newest product launches from Nike"
- "How many credits do I have left?"

## Authentication

This plugin uses OAuth to connect to your Particl account. Your existing export credits are used for MCP queries (1 credit per data row for most tools, some tools are free).
