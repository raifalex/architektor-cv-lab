# ARCHITEKTOR CV & Career Studio

Browser-based CV analysis and career exploration with transparent deterministic rules. No AI API, API key, or server is required. Career directions are suggestions based on CV evidence, not predictions or psychological diagnoses.

Optional personal service by Alex Raif: extended analysis plus a 30-minute conversation, USD $20 total, one time. Contact, payment and scheduling are arranged directly through the site WhatsApp link.

## Source and deployment

`ARCHITEKTOR_GitHub_Pages.zip` contains the complete editable source, tests, dependency lockfile, licenses, setup instructions and tested production `dist/`. Extract it to work on the project. The root `.github/workflows/pages.yml` extracts this archive, runs the analysis tests and deploys `dist/` to GitHub Pages.

To update: extract the archive; use Node 22.13 or newer and pnpm 11.25.0; run `pnpm install --frozen-lockfile --ignore-scripts`, `pnpm test` and `pnpm build`. Repackage the `ARCHITEKTOR_GitHub_Pages/` folder including the updated `dist/` and excluding `node_modules` and `.git`, then replace the root ZIP. The workflow publishes the bundled build; it does not rebuild source automatically.

CV processing stays in the browser. Cases are stored locally only when explicitly saved. Saved cases on another domain do not migrate automatically. Never commit CVs, personal case data or secrets to this public repository.
