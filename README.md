# Amazon NEXT

Premium responsive marketplace demo configured for **GitHub Pages**.

## Open the live website
After the first successful workflow run, the site is published at:
https://pugartj-a11y.github.io/my-shopp/

## Automatic deployment
Every push to the `main` branch runs `.github/workflows/deploy-pages.yml` and publishes the `public/` folder. You can also start deployment manually from the **Actions** tab.

If the first deployment does not start, open **Settings → Pages** in the repository and set **Build and deployment → Source** to **GitHub Actions**.

## Run locally
No Node.js or build step is required for the GitHub Pages version. Open `public/index.html` in a browser, or use VS Code Live Server.

The Express server remains available as an optional local development backend:
```bash
npm install
npm start
``

## Included demo features
- Responsive product catalogue, search, categories and sorting
- Shopping bag saved in browser localStorage
- Compare up to four products
- Keyword-based shopping helper (not a connected LLM)
- Image-picker demo with category matching (no image recognition or upload)
- Price-alert notes saved in browser localStorage (no automatic price monitoring or email)

## GitHub Pages limitations
GitHub Pages serves static files only. It cannot run `server.js`, Express routes, scheduled jobs, databases, payment processing, email delivery or private API keys. Real AI, image recognition, user accounts, live price tracking and notifications need a separate backend service.

This is an independent demo with fictional sample product data and is not affiliated with Amazon.
