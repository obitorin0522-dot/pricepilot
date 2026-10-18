# PricePilot MVP v2

A beginner-friendly, responsive shopping-comparison prototype. Built with plain HTML, CSS and JavaScript to keep the project lightweight and free to run locally.

## Features
- Search across sample products and filter by category
- Sort by lowest/highest price or name
- Compare retailer offer examples for a specific variant
- Wishlist and target price saved in localStorage
- Responsive layout and installable PWA foundation
- Basic offline shell caching when served over HTTP(S)
- Clear disclosure that product and retailer data are fictional sample data

## Run locally
1. Extract the ZIP.
2. Open the folder in VS Code.
3. Use the Live Server extension to open `index.html`.
   - Or run `python -m http.server 8000` from this folder and open `http://localhost:8000`.

## Install on Android
Host the files on an HTTPS static host. Open the URL in Chrome on Android and choose Install app / Add to Home screen when available. A browser install is not the same as publishing a native app on Google Play.

## Current limitations
- Retailer names, offers, and price history are illustrative only.
- No live retailer API, affiliate feeds, login, cloud sync, server-side price tracking, or push notifications.
- The wishlist and target prices are stored on the current browser/device.
- The history graph is a visual placeholder and must not be interpreted as real historical data.

## Next architecture
Frontend: responsive PWA (this prototype)
Backend: Supabase or another free-tier database for canonical product/variant records, retailer offers, price snapshots, and user watchlists.
Price ingestion: authorized retailer APIs/affiliate feeds; scheduled backend jobs; validation and freshness timestamps.
Reliability: schema validation, request timeouts, retry/backoff, stale-data labels, automated tests for variant matching and total-price calculations.
Android: initially use the installable PWA; later consider Capacitor or a native app if there is a clear need.
