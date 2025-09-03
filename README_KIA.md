# Quirk Kia — Sight-Unseen Trade-In Appraisal


## What was changed automatically
- All obvious dealership names and URLs retargeted to **Quirk Kia** and **https://www.quirkkiasouth.com/**.
- "Back to Quirk …" links updated.
- Common CDJR references replaced with Kia.

Total files touched: 5 (subs: 24).

## What you still need to do
1. **Logos/Branding**
   - Replace any brand-specific assets with Kia versions if you see CDJR or Mopar marks.
   - Suggested files to add (if not present):
     - `assets/kia.svg` (Kia brand mark)
     - `assets/quirk-kia.svg` (Quirk Kia lockup)
   - In `assets/app.js`, the logo injector looks for a Quirk logo; if you want a Kia oval/wordmark too, add it to the DOM next to the Quirk logo or swap the path.

2. **Return/Home Links**
   - Confirm any links point to `https://www.quirkkiasouth.com/`. We replaced common variants, but double-check success page and header/footer.

3. **Email recipients (Netlify function)**
   - Open `netlify/functions/trade-appraisal.js` and set the **To** recipients for Kia.
   - If the function relies on Netlify environment variables, set them in your new site:
     - `SENDGRID_API_KEY`
     - `TRADE_TO_EMAIL` (or equivalent, depending on the file)
     - `FROM_EMAIL`

4. **Deploy**
   - Create a new GitHub repo (e.g., `quirk-trade-appraisal-kia`), commit/push this folder.
   - Create a new site in Netlify and connect that repo.
   - Set the environment variables above, then deploy.
   - Optional: set a custom domain like `quirkkiatrade.netlify.app` or connect a subdomain.

## Notes
- We performed case-insensitive text substitutions. If you spot a lingering "Marshfield" or "CDJR", search the codebase and update it.
- Feel free to rename the site title in `index.html` and any `<meta>` tags if needed.
