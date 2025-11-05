
# ToolVerse — Bundle

This bundle contains:
- `index.full.html` - full single-page site (15 tools) using Tailwind + Vanilla JS (client-side). Drop into any static host.
- `index.html` - lightweight entry with links to the full file.
- React scaffold (`/react-app`) with Vite config (minimal).
- Server backend (`/server`) that provides a caching endpoint for currency conversion.
- `sitemap.xml` and `robots.txt`.
- `README.md` (this file).

## Quick static deploy (GitHub Pages)
1. Create a new repository on GitHub and push these files to the `main` branch.
2. Rename `index.full.html` to `index.html` (if you want it as root) or keep current structure.
3. In repo Settings → Pages: select branch `main` and root `/` (or `/docs` if you prefer).
4. Save — your site will be published at `https://<your-username>.github.io/<repo>/`.

## Quick deploy (Netlify)
1. Drag & drop the ZIP contents into Netlify Deploy (or connect repo).
2. For client-only site, Netlify will serve `index.html` from the root.
3. To use the server backend, deploy `/server` separately as a serverless function or on Heroku/Vercel/Render and update the client currency endpoint to point to your server URL.

## Running the Node backend locally
```bash
cd server
npm install
node server.js
# server listens on http://localhost:3000
# Example: http://localhost:3000/api/convert?from=USD&to=PKR&amount=10
```

## React scaffold
```bash
cd react-app
npm install
npm run dev
```

## Notes & next steps
- Replace the Google Analytics ID `G-XXXXXXX` in the HTML with your real GA4 measurement ID.
- Update `sitemap.xml` and `robots.txt` with your real domain.
- Consider moving to a proper CDN and building Tailwind locally for production performance.
- If you want, I can also prepare CI/CD (GitHub Actions) to auto-deploy on push.
