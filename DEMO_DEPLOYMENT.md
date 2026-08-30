# Gulf Store demo deployment

This release is ready to deploy as a Vercel static demo. The storefront uses its built-in catalog fallback and browser cart when the MySQL API is unavailable, so clients can browse products and submit a demo order request.

## GitHub

1. Create a new empty repository on GitHub (for example `gulf-store-demo`).
2. Open a terminal in this folder and run:

```bash
git init
git add .
git commit -m "Prepare Gulf Store demo"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/gulf-store-demo.git
git push -u origin main
```

Do not commit `backend/.env` or any production credentials.

## Vercel

1. Sign in to Vercel and choose **Add New → Project**.
2. Import the GitHub repository.
3. Framework preset: **Other**.
4. Build command: leave empty.
5. Output directory: leave empty (project root).
6. Deploy.

The Vercel demo is frontend-only. MySQL, XAMPP, Razorpay and the production admin API should be connected later through a hosted backend/database; they cannot use `localhost` from Vercel.
