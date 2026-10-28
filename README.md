# College Cyber Governance, Audit & Compliance Management System

CGACMS is a React prototype for centralizing cybersecurity governance work at a college. It brings staff lifecycle, access review, asset recovery, license tracking, audit management, risk tracking, and compliance evidence into one workspace.

> **Prototype notice:** This repository contains a client-side demo with sample records. Records are saved to the browser's local storage and uploaded evidence is saved in that browser's IndexedDB. There is no server, authentication, authorization enforcement, shared database, or backup. Do not enter real staff, student, security, or compliance data. GitHub Pages is suitable for previewing this frontend, not for operating the institution's production governance system.

## Features

- Governance dashboard with current audit, risk, license, and compliance summaries.
- User and role directory with activate/suspend controls and a role-permissions matrix.
- Staff onboarding workflow with checklist progression.
- Staff offboarding workflow with access revocation and asset-return tracking.
- Asset inventory with assignment, availability filters, and CSV export.
- Access registry with Active, Pending, Privileged, and Dormant views; pending requests can be approved or denied.
- Software license inventory with seat assignment and reclamation.
- Audit views for Active, Completed, and Scheduled audits, including start and closure actions.
- Risk register with likelihood × impact scores, filters, and treatment status.
- Compliance control register with local evidence upload and download.
- Governance activity trail for changes made in the current browser.
- CSV export from each data module.
- Responsive layout based on the supplied CGACMS design references.

## Technology

- React 19
- Vite 8
- Browser local storage for prototype records
- IndexedDB for uploaded evidence files
- GitHub Actions and GitHub Pages for static preview deployment

## Requirements

- Node.js 22.12 or newer (Node.js 22 LTS recommended)
- npm, included with Node.js

## Run locally

### First-time setup

Clone the repository and enter the project folder:

```powershell
git clone https://github.com/aashay-d12/CGACMS.git
cd CGACMS
```

If you already have this project folder, open PowerShell in that folder and continue with the install step.

### Start the app

Open PowerShell or a terminal in the project directory and run:

```powershell
npm install
npm run dev
```

Open the URL printed by Vite. By default, it is `http://localhost:5173/`.

To create and serve the production build locally:

```powershell
npm run build
npm run preview
```

The production files are written to `dist/`. The `dist/` directory is generated and should not be committed.

## Push changes to GitHub

This project is connected to [github.com/aashay-d12/CGACMS](https://github.com/aashay-d12/CGACMS). From the project folder, run these commands after making changes:

```powershell
git add README.md package.json package-lock.json src .github
git commit -m "Improve CGACMS governance workflows"
git push origin main
```

GitHub will request authentication if this computer is not already signed in. For a fork or a different remote, update the clone URL and remote name to match that repository.

## Publish a preview with GitHub Pages

The workflow in `.github/workflows/deploy-pages.yml` builds and deploys the Vite app whenever you push to `main`.

1. Push the repository to GitHub using one of the methods above.
2. In the repository, open **Settings → Pages**.
3. Set **Build and deployment → Source** to **GitHub Actions**.
4. Open **Actions** and wait for **Deploy CGACMS to GitHub Pages** to finish.
5. Open the published URL shown by the deployment job. For this repository it is `https://aashay-d12.github.io/CGACMS/`.

The Vite configuration sets the repository subpath during the GitHub Actions build, so assets load from the correct Pages URL.

## Project structure

```text
CGACMS/
├── .github/workflows/deploy-pages.yml  # GitHub Pages deployment
├── src/
│   ├── App.jsx                         # Modules, workflows, and local demo data
│   ├── main.jsx                        # React entry point
│   └── styles.css                      # Responsive application styling
├── index.html
├── package.json
├── package-lock.json
└── vite.config.js
```

## Useful commands

| Command | Description |
| --- | --- |
| `npm install` | Install project dependencies |
| `npm run dev` | Start the development server |
| `npm run build` | Build the static production app |
| `npm run preview` | Serve the production build locally |

## Production roadmap

Before using CGACMS with institutional data, add a backend API, PostgreSQL database, authentication and server-enforced role permissions, audit logging, backups, and controlled evidence storage. The current local browser storage is for demonstration only and does not synchronize between staff or devices.
