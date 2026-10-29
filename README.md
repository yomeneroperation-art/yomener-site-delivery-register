# Yomener Site Delivery Register
Mobile-first installable web app for delivery registration, stock records, and weekly/monthly/quarterly summaries.

## Deploy
GitHub Actions workflow in `.github/workflows/pages.yml` deploys this repository to GitHub Pages on pushes to `main`. Enable **Settings → Pages → Build and deployment → GitHub Actions** if needed. Expected URL: https://yomeneroperation-art.github.io/yomener-site-delivery-register/

## Backend
Supabase project: `vmqcoubkjlgkkcqgnilt`. Public URL and publishable key are in `supabase-config.js`; these are client-side identifiers, not service-role credentials. Never add a service-role/secret key to this public repository.

## Required before company use
1. Disable public sign-ups in Supabase Auth; create named accounts for the intended colleagues.
2. Enable Realtime for `deliveries` and `stock_records` if live updates do not appear.
3. Test signed-out access, cross-user updates/deletes, two-phone sync, offline entry, and reconnect sync.
4. Open the hosted app online once before using offline mode. Pending new entries are stored locally; offline edits/deletes and stock-consumption/transfer ledger features are not included in this first version.
5. This is a PWA, not an Android APK or iOS App Store build. Use HTTPS, then choose Add to Home Screen on phones.
