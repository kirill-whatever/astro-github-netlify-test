# Astro → GitHub → Netlify Test Site

A deliberately simple three-page Astro test project:

- `/` — HELLO
- `/picture/` — uploaded photo
- `/goodbye/` — GOODBYE

All pages share the same top navigation.

## Requirements

- Node.js 22.23.4 or newer compatible even-numbered release
- VS Code
- Git
- GitHub account
- Netlify account

## Run locally

Open this folder in VS Code, then open **Terminal → New Terminal** and run:

```bash
npm install
npm run dev
```

Open the local address shown by Astro, normally:

```text
http://localhost:4321/
```

Stop the development server with `Ctrl+C`.

## Production build test

```bash
npm run build
npm run preview
```

Astro creates the production site inside `dist/`.

## GitHub

Create an empty GitHub repository, then from this project folder run:

```bash
git init
git add .
git commit -m "Initial Astro test site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

If your existing GitHub workflow creates the repository for you, use its supplied remote URL instead.

## Netlify

In Netlify:

1. Add a new project/site.
2. Import an existing project.
3. Choose GitHub and select this repository.
4. Netlify should detect Astro automatically.
5. Confirm:
   - Build command: `npm run build`
   - Publish directory: `dist`
6. Deploy.

The included `netlify.toml` already contains the build command, publish directory, and Node version.

After the initial connection, every new push to the production branch will cause Netlify to build and deploy the latest version automatically.
