# Amazon NEXT

A static premium marketplace demo. The site opens directly from the root `index.html`.

## Live website
https://pugartj-a11y.github.io/my-shopp/

## GitHub Pages deployment
The workflow `.github/workflows/deploy-pages.yml` publishes the repository root on every push to `main`. In repository Settings → Pages, choose **GitHub Actions** as the deployment source.

## Project files
- `index.html` — website entry point
- `styles.css` — responsive styling
- `app.js` — browser interactions and localStorage
- `products.js` — demo product catalogue
- `.github/workflows/deploy-pages.yml` — automatic deployment

No Node.js installation or build command is required. GitHub Pages serves `index.html` automatically.

## Demo limitations
Cart, compare list and price-alert notes are saved in the current browser only. The shopping helper uses simple keyword matching. Image search is a category-based demo, not image recognition. No live prices, email alerts, account system, payments or server-side AI are connected.

Independent demo project; not affiliated with Amazon.
