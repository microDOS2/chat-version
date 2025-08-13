
# microDOS(2) Static Website

This is a fully self-contained, multi-page static site with a working **client-side checkout** that captures orders into `localStorage` and an **Admin dashboard** to view/search/export those orders.

## Files
- `index.html` — Landing, pricing, and checkout (3-step, validated).  
- `metocin.html` — What is Metocin (4‑HO‑MET): overview and specs.  
- `microdosing.html` — Visual microdosing guide (pure CSS).  
- `stories.html` — User stories with fallbacks for images.  
- `admin.html` — Admin: view, filter, export CSV; clear demo data.

## Deploy to GitHub Pages
1. Create a new repository (public).  
2. Upload all files from this folder. Ensure the default page is `index.html`.  
3. In **Settings → Pages**, set Source to **Deploy from a branch**, and select the `main` branch, `/root` folder. Save.  
4. Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

## Swap in your assets
- Replace YouTube URLs in `index.html` (search `videoSources`).  
- Adjust pricing/plan IDs in the Pricing block if needed.  
- Replace images on `stories.html` or keep the placeholder fallback.

## Wire real payments (Stripe, Paddle, etc.)
This is a front-end only build. To go live with payments:
- Replace the Step 2 card fields with your payment provider’s drop-in elements.  
- On success, POST the order payload to your backend and store it in your database.  
- Remove the `paid_simulated` bits and use real transaction IDs.

## Compliance
- Add your real **Terms of Service** and **Privacy Policy** and link them in the footer.  
- Verify shipping restrictions and age gates per jurisdiction.
