LOOTVault V2 — TON Connect frontend package

Upload all three runtime files to the same public HTTPS website root:
- index.html
- tonconnect-manifest.json
- lootvault-logo.png

Edit tonconnect-manifest.json before publishing. Replace both occurrences of
https://REPLACE-WITH-YOUR-PUBLIC-APP-DOMAIN with the real public HTTPS origin
where the app is hosted (for example https://your-app.example.com).

The manifest must be reachable at /tonconnect-manifest.json and the logo at
/lootvault-logo.png. The HTML loads TON Connect UI from unpkg CDN and requests
the manifest from its own origin.

This adds real TON Connect wallet linking/address display and disconnect.
It does not yet persist the connected address to Supabase/backend. Backend
wallet persistence and withdrawal request integration remain required.
