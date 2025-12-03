# MUI Joy Messages on GitHub Pages

This project hosts the MUI Joy UI "Messages" template with a GitHub Pages workflow so it can be deployed automatically from the `main` branch.

## Running locally
1. Install dependencies
   ```bash
   npm install
   ```
2. Start the dev server
   ```bash
   npm run dev
   ```
3. Build for production (used by GitHub Pages)
   ```bash
   npm run build
   ```

## Deployment
A GitHub Actions workflow builds the site and publishes the `dist` folder to GitHub Pages whenever `main` is updated. The Vite config sets `base: '/MUI/'` to match the repository name; adjust it if you fork the repo under a different name.
