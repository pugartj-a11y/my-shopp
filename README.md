# Amazon NEXT

A premium, responsive full-stack marketplace prototype. This is an independent demo and is not affiliated with Amazon.

## Features
- Responsive storefront with search, categories, sorting and product cards
- Product bag/cart demo
- Product comparison (up to four products)
- AI shopping assistant demo endpoint (catalogue keyword matching; no external LLM required)
- Image upload visual-search demo endpoint (category-based matching; connect a vision model for semantic image recognition)
- Price alert creation and server-side JSON persistence
- Express API and seeded catalogue

## Requirements
- Node.js 18+

## Run locally
```bash
npm install
npm start
```
Open http://localhost:3000

## API
- `GET /api/health`
- `GET /api/products?q=&category=&sort=`
- `GET /api/products/:id`
- `GET /api/compare?ids=p1,p2`
- `POST /api/assistant` JSON `{ "message": "..." }`
- `POST /api/visual-search` multipart form: `image`, optional `category`
- `POST /api/price-alerts` JSON `{ "productId":"p1", "targetPrice":150, "email":"you@example.com" }`
- `GET /api/price-alerts`

## Production integrations still required
The demo deliberately does not collect payment details or claim real Amazon inventory. Before production, add:
1. Authentication and authorization (e.g. Auth.js or managed identity provider).
2. PostgreSQL and migrations instead of `data.json`.
3. A compliant product data source / seller catalogue API and scheduled price updates.
4. A real LLM provider for grounded AI recommendations and moderation.
5. A vision model and secure image storage for semantic visual search.
6. Email provider + background jobs for price notifications.
7. Payment provider hosted checkout, tax, shipping and refund workflows.
8. Rate limiting, CSRF protection where applicable, validation, logging, tests, backups and monitoring.

## Notes
- `data.json` is seeded demo data. Do not use it as a multi-user production database.
- Uploaded visual-search images are deleted after the demo request.
- Product names and prices are fictional sample catalogue data.
