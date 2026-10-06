# Silveroak Law Firm

Standalone copy of the existing live website, separated from Deborah's portfolio. HTML, inline CSS/JavaScript, and local images were recovered from the published website because the supplied GitHub repository does not contain this project's source.
## Run locally

Install Node.js 22 or newer. No npm dependencies are required.

```bash
npm run dev
```

Open http://localhost:3000. Use another port with `PORT=3001 npm run dev` on macOS/Linux or `$env:PORT=3001; npm run dev` in PowerShell.

## Build

```bash
npm run build
```

The build copies `public/` into `dist/`. No API keys or environment variables are required for the current front end.

## Push to its own GitHub repository

Extract this ZIP, open the `silveroak-law` folder, and create an empty GitHub repository named `silveroak-law` (without an initial README).

```bash
git init
git add .
git commit -m "Initial standalone Silveroak Law Firm website"
git branch -M main
git remote add origin https://github.com/blackdebbie/silveroak-law.git
git push -u origin main
```

## Deploy separately to Vercel

Import that GitHub repository as a new Vercel project. Set framework preset to **Other**, root directory to the repository root, build command to `npm run build`, and output directory to `dist`. `vercel.json` supplies the build settings. Deploy. The homepage is `/`, and existing `.html` page URLs remain available.

## Pages included

- `/about.html`
- `/blog.html`
- `/case-studies/case-study-5.html`
- `/consultation.html`
- `/contact.html`
- `/practice.html`

## Existing behavior and dependencies

Contact and consultation forms are front-end interfaces without a submission backend. Placeholder social links retain their original behavior.

External Google Fonts, icon libraries, and Unsplash/avatar image URLs remain as in the original website and require internet access. All discovered local page and image dependencies are bundled. This package does not include a server, database, payment integration, or hidden application source.

## Validation

- Static build completed.
- All internal HTML navigation and image references resolve to included files.
- 7 inline JavaScript blocks passed Node syntax checks.
- Interactive browser verification was unavailable in this environment; test mobile navigation, forms, and external assets in a Vercel preview before using with clients.

See `SOURCE-NOTES.json` for the recovered file inventory and source URL.
