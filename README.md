# Rakshak frontend demo

This is a static, frontend-only demonstration of Rakshak. It parses `.eml` text in the browser, applies transparent deterministic rules, stores up to 20 results in local browser storage, and supports browser printing to PDF.

It does not call DNS, RDAP, geolocation, reputation, Gmail, Outlook, Gemini, or authentication-verification services. Those features require the full FastAPI application.

## Run locally

```powershell
pnpm install
pnpm build
pnpm preview
```

## Deploy on Vercel

Import this folder as a Vercel project. Use the Vite preset, build command `pnpm build`, and output directory `dist`. No environment variables are required.

## Direct static upload

Upload the contents of `dist` (including its `assets` folder). The source index.html needs Vite to compile TypeScript and must not be uploaded by itself. The ready-to-upload ZIP contains only compiled files. Keep index.html and assets together. Serve over HTTPS; opening index.html directly from File Explorer is not supported.
