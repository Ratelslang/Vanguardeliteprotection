# Vanguard Elite Protection — GitHub Pages backup

This folder is a static export of the Vanguard Elite Protection website. It includes the compiled React site, local images, the company-profile PDF, and a `404.html` fallback for client-side routes such as `/services`, `/assessment`, `/areas`, `/insights`, `/privacy`, and `/terms`.

## Fastest publishing option: user site

Create a repository named `<your-github-username>.github.io`, extract the contents of this export into the repository root, commit the files, and push to the `main` branch. In the repository, open **Settings → Pages**, choose **GitHub Actions** if prompted, and wait for the Pages deployment to complete. The root-compatible build in this ZIP is intended for this user-site or custom-domain arrangement.

## Project-site option

For a normal repository such as `vanguard-elite-protection`, use the source project’s included workflow at `.github/workflows/deploy.yml` instead of uploading only this compiled ZIP. The workflow builds with `VITE_BASE_PATH=/<repository-name>/`, updates the SPA fallback, and publishes the `dist/public` artifact through GitHub Pages. Copy the source project to your GitHub repository, ensure the default branch is `main`, push it, then enable **Settings → Pages → Source: GitHub Actions**.

## Contact behavior and offline scope

The website is static and does not require the Manus server to render pages. Consultation forms, WhatsApp actions, email links, telephone links, the brochure download, cookie choice, service pages, assessment flow, operating-area page, and insight articles remain available in the export. WhatsApp, email, telephone, and external map links naturally require the visitor’s device or network to be online when they are used.

The export does not include the Manus database, OAuth, server-side APIs, or Manus analytics services. No enquiry is stored by the static website itself; the contact journeys hand the visitor’s chosen information to WhatsApp, email, or telephone only after the visitor chooses that action.

## Updating the backup

When the Manus-hosted site changes, rebuild the project with `VITE_BASE_PATH=/` for a root-compatible ZIP, or push the source project to GitHub and let the included Actions workflow rebuild the project-site version automatically.
