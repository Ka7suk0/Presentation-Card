# Svelte Contact Card

A small, responsive personal contact page built with Svelte and Vite.

## Requirements

- Node.js 18+
- npm

## Run locally

```bash
npm install
npm run dev
```

Open the local URL printed by Vite.

## Customize

Edit `src/App.svelte`:

- `name` and `role`
- `interests`
- `links` (replace the URLs)
- The professional profile text

For the CV link, put your PDF in the `public/` folder and update the link to its filename, for example `/cv.pdf`.

## Build

```bash
npm run build
npm run preview
```

The production site is generated in `dist/`.

## Deploy to GitHub Pages

You can deploy the generated `dist/` directory using GitHub Pages with GitHub Actions. If the repository is published under `https://username.github.io/repository-name/`, configure Vite's `base` option in `vite.config.js` to `'/repository-name/'` before building.
