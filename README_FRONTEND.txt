LOOTVault V2 Frontend
=====================

Files:
- index.html: the current LOOTVault V2 frontend supplied for this project.

Deployment:
1. Upload this folder to your frontend GitHub repository.
2. Keep the HTML filename as index.html.
3. Deploy the repository using Vercel.
4. Set the final frontend URL in the HOKAS backend CORS_ORIGINS environment variable.
5. Do not test payments until the frontend API calls have been matched and tested against the deployed backend.

Important:
This package contains the frontend HTML only. It is not yet fully integrated with the updated HOKAS backend.
The HTML currently leaves LOOT_API_BASE_URL and LOOT_API_ENDPOINTS configurable at runtime, and the backend API contract still needs an integration pass before live mining, payment, contest, and withdrawal actions can be relied upon.

Keep all bot tokens, Toncenter API keys, and database credentials on the backend. Never place them in this frontend.
