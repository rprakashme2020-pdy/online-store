# Reusable Ecommerce Product

This package contains a standalone Node.js + MySQL ecommerce application that can be connected to any existing website.

## Install locally

1. Install Node.js 20+ and MySQL (XAMPP is suitable for local development).
2. Copy `backend/.env.example` to `backend/.env` and set database credentials.
3. Import `backend/database/schema.sql` into a new database.
4. Apply migrations in `backend/database/migrations/` in order.
5. Run `npm install` inside `backend/`.
6. Run `npm run seed` if starting with the included catalog.
7. Run `npm start` and open the configured storefront.

## Configure a new business

Copy `config/store.config.example.json` to `config/store.config.json`. Set the business name, logo, colors, contacts, delivery areas, currency, and payment methods. Keep passwords and API keys in environment variables, never in this JSON file.

## Connect an existing website

Link to the storefront with a normal URL (`https://shop.example.com/products.html`) or embed a future storefront widget. The existing site can remain unchanged while this package runs on a subdomain or `/shop` path.

## Production deployment

Create a separate database and subdomain, upload the package, configure the cPanel Node.js application startup file as `backend/server.js`, set environment variables, and test before switching any primary-domain files.
