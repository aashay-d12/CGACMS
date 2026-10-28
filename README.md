# College Cyber Governance, Audit & Compliance Management System

CGACMS is a React prototype for managing cybersecurity governance workflows at a college. The interface includes dashboard, users and roles, staff onboarding and offboarding, asset inventory, access governance, software licenses, audits, risks, and compliance tracking.

The current version is a frontend prototype with sample records. Asset records are saved in the current browser using local storage. Authentication, shared database storage, and real approval integrations are not connected yet.

## Run locally

1. Install Node.js 22 or newer from [nodejs.org](https://nodejs.org/).
2. Open PowerShell or a terminal in the project folder.
3. Install the project dependencies:

   ```powershell
   npm install
   ```
4. Start the development server:

   ```powershell
   npm run dev
   ```
5. Open the local URL printed in the terminal, usually `http://localhost:5173/`.

To create and preview a production build locally:

```powershell
npm run build
npm run preview
```

## Deploy on GitHub

In the project folder, run:

   ```powershell
   git init
   git add .
   git commit -m "Build CGACMS governance prototype"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/CGACMS.git
   git push -u origin main
   ```

Replace `YOUR-USERNAME` with your GitHub username.

## Publish on GitHub Pages

The included workflow at `.github/workflows/deploy-pages.yml` builds and publishes the site whenever you push to `main`.

1. Push the repository to GitHub using one of the methods above.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, set the source to **GitHub Actions**.
4. Open the **Actions** tab and wait for **Deploy CGACMS to GitHub Pages** to complete.
5. Open the published URL shown in the workflow’s deployment job. It will usually look like `https://YOUR-USERNAME.github.io/CGACMS/`.

Future updates publish automatically when committed and pushed to `main`:

```powershell
git add .
git commit -m "Describe your update"
git push
```

## Main commands

| Command             | Purpose                                 |
| ------------------- | --------------------------------------- |
| `npm install`     | Install dependencies                    |
| `npm run dev`     | Start the local development server      |
| `npm run build`   | Create the production site in `dist/` |
| `npm run preview` | Preview the production build locally    |
