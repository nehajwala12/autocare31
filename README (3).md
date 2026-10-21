# Ares commercial diligence: password-protected site

`index.html` is CreditSwan's commercial diligence for Ares Management, dated 20 October 2026, with the Monro term-sheet section.

- **Password:** `AutoCare2026`
- The report inside `index.html` is encrypted (AES-256-GCM, key derived from the password). Without the password the file shows only a sign-in screen, whether it is served from Vercel, opened from disk or forwarded by email.
- The password is asked each time the page is opened in a new tab or window.
- Use a current version of Chrome, Edge, Safari or Firefox.

## Deploy to Vercel

1. In this folder, run `npx vercel --prod` and create a new project (framework preset: Other; no build command; output directory: the folder root).
   Or drag this folder into vercel.com/new.
2. Open the address Vercel gives and enter the password.

No environment variables, build step or dependencies are needed. `vercel.json` sets `noindex` and `no-store` headers, and `robots.txt` blocks crawlers.

## Change the password

The password is built into the encrypted file, so changing it means producing a new `index.html` from the report.
