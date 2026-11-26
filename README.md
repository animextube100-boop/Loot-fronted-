# LOOTVault V2 — Frontend

## Structure

```text
LOOTVault_V2_Frontend/
├── index.html                 # Complete responsive Mini App interface
├── config/
│   └── config.js               # Backend URL and API route configuration
├── assets/
│   └── lootvault-logo.png      # Extracted app logo asset
├── tonconnect-manifest.json    # TON Connect app manifest
└── README.md
```

## Deploy

1. Upload the contents of this folder to the root of the frontend GitHub repository (not the enclosing ZIP folder).
2. Deploy/redeploy on Vercel. The entry page is `index.html`.
3. Keep `tonconnect-manifest.json` and `assets/lootvault-logo.png` at the shown paths.
4. The configured backend is `https://app-ff4dfd.subhub.tr`.

## Telegram authentication fix

The account bootstrap now calls `POST /api/account` (not GET) and sends Telegram Mini App `initData` in both `X-Telegram-Init-Data` and `Authorization: tma ...`, plus the JSON `init_data` field. The app must be opened from the `@LOOTVaultV2Bot` Mini App button; a normal browser visit does not provide valid Telegram init data.

## Important backend integration status

The currently confirmed account route is `POST /api/account`. The other endpoint settings are intentionally blank until their exact routes and request/response schemas are confirmed in the deployed backend `/docs`. Consequently, payment, claim, withdrawal-history, and contest actions remain safely unavailable rather than pretending to complete. Do not enable real TON payments until the backend creates unique payment intents and independently verifies the on-chain transaction on TON Mainnet.

The frontend retains the existing LOOTVault V2 design and screens, including mining, miner upgrades, daily rewards, community tasks, contest, profile, TON Connect, and withdrawal UI.
