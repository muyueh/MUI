# Joy UI Messages template on GitHub Pages

This project packages the [Joy UI Messages template](https://github.com/mui/material-ui/tree/master/docs/data/joy/getting-started/templates/messages) into a Vite + React app that can be deployed to GitHub Pages without committing built assets or other binaries.

## Local development
1. Install dependencies (uses the provided `package-lock.json`):
   ```bash
   npm ci
   ```
2. Start the dev server:
   ```bash
   npm run dev
   ```
3. Build locally (optional):
   ```bash
   npm run build
   ```
   The production files are emitted to the `docs/` folder (ignored by Git) so you can preview with `npm run preview` and then delete the folder before committing.

## GitHub Pages deployment
A workflow is included to build and deploy the site without checking in generated assets:

- GitHub Actions file: `.github/workflows/deploy.yml`
- Output folder: `docs/`
- Build command: `npm ci && npm run build`

Enable GitHub Pages with **Source = GitHub Actions** in your repository settings. Each push to `main` (or a manual run) will build the app and publish the contents of `docs/` to the Pages site. Because the build output is produced in the workflow and not committed, the repository remains free of binary files.
