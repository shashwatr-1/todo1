# Exam Prep — To‑Do & Error Log (Vite + React)

This repo includes a GitHub Actions workflow that deploys to Netlify on every push to `main`.

## Dev
```bash
npm install
npm run dev
```

## Build
```bash
npm run build
```

## Netlify Deploy via GitHub Actions

1. Create a site on Netlify (or use an existing one). Copy the **Site ID** from Site settings → General → Site details.
2. In your GitHub repo → Settings → Secrets and variables → Actions → **New repository secret**:
   - `NETLIFY_AUTH_TOKEN` → from Netlify User settings → Applications → Personal access tokens.
   - `NETLIFY_SITE_ID` → from the Site settings (step 1).
3. Push to `main`. The workflow will build and deploy with Netlify CLI.

If you prefer using Netlify’s Git provider integration instead of Actions, you can remove `.github/workflows/netlify-deploy.yml` and connect the repo in Netlify UI.
