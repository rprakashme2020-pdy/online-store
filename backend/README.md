# Baruch Engineers local commerce backend

This backend is designed for the GoDaddy cPanel Node.js App + MySQL setup.

## Local setup

1. Install Node.js 20+ and MySQL (XAMPP is fine for local development).
2. Copy `.env.example` to `.env` and set the local MySQL credentials.
3. Run `mysql -u root -p < database/schema.sql`.
4. Run `npm install` in this folder.
5. Run `npm run seed` to import the 78 Gulf products.
6. Run `npm start` and open `http://localhost:3000/products.html`.

The frontend falls back to its local catalog when opened directly from disk, and automatically uses `/api/products` and `/api/orders` when served by this Node app.

## GoDaddy deployment notes

Create the MySQL database/user in cPanel, import `database/schema.sql` through phpMyAdmin, upload the project, set the Node.js App entry point to `backend/server.js`, set the environment variables from `.env.example`, and start the app. Never upload a real `.env` file to a public repository.

Razorpay is intentionally not included yet.
