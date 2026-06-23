# Crave Shopify MCP

MCP server for Crave Bake Supply. It connects ChatGPT to Shopify product data so products can be reviewed for Florida sales tax setup and product category cleanup.

## Tools

- `list_products`: lists products, product types, tags, categories, variants, and a Florida tax suggestion.
- `update_product_type`: changes a product type after owner confirmation.
- `update_product_tags`: replaces product tags after owner confirmation.
- `set_variant_taxable`: changes a variant taxable flag after owner confirmation.

## Render Settings

Use these values in Render:

- Language: `Node`
- Branch: `main`
- Build Command: `npm install`
- Start Command: `npm start`

## Environment Variables

Add these in Render under Environment:

```text
SHOPIFY_SHOP=cravebakesupply.myshopify.com
SHOPIFY_CLIENT_ID=your_client_id
SHOPIFY_CLIENT_SECRET=your_client_secret
SHOPIFY_API_VERSION=2026-04
MCP_AUTH_TOKEN=make-a-long-private-password
```

Do not put secrets in GitHub.

## MCP URL

After Render deploys, the MCP URL will be:

```text
https://YOUR-RENDER-SERVICE.onrender.com/mcp
```

Use Bearer token authentication with the value from `MCP_AUTH_TOKEN`.
