# Somatic Flow — information page

Public landing page and privacy policy for the Somatic Flow Android app by Reliable IT, served by GitHub Pages:

- Landing page: https://diegoeg78.github.io/somatic-flow-privacy/ (`index.html`)
- Privacy policy: https://diegoeg78.github.io/somatic-flow-privacy/privacy/ (`privacy/index.html`)

The app's source is in the private repo `diegoeg78/somatic-flow`. The privacy policy there (`client/public/privacy.html`, bundled in the app) is the source of truth; keep `privacy/index.html` here in sync with it.

## When the app is published on Google Play

1. **Play link:** in `index.html`, replace the "Coming soon to Google Play" `<span>` with the link in the HTML comment above it.
2. **Domain:** point `somaticflow.reliableits.net` here:
   - At the DNS provider for reliableits.net, change the `somaticflow` record to a **CNAME** pointing to `diegoeg78.github.io`.
   - In this repo: **Settings → Pages → Custom domain** → `somaticflow.reliableits.net` → Save. GitHub adds a `CNAME` file.
   - Once the certificate is issued (can take up to an hour), tick **Enforce HTTPS**.
   - The github.io URLs then redirect to the custom domain, so links already given to Play Console keep working.
3. **Retire the old web app** on portal-server-01 (steps in `docs/TAKEOVER_PLAN.md` in the app repo).
