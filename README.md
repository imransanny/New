# TOMATO Clothing — fixed GitHub Pages release

## Fix for stuck “Preparing your experience…” screen

Upload **`app.html`** in this folder, replacing your old `app.html` at the repository root. This fixed file contains its own styling, JavaScript and demo product photos. **Do not rename it** and do not upload the ZIP itself to GitHub.

Check your live site at `https://YOUR-USERNAME.github.io/YOUR-REPO/app.html?mode=login`. If it still displays the old loader, wait for GitHub Actions / Pages to complete and refresh the page. You may add `?mode=login&v=2` to bypass an older cached URL.

For full storefront support, upload **all project files and `assets/`**, preserving the current folder structure. `index.html` is the public store, `app.html` the standalone role demo. The homepage's Login, Signup and 4-Roles links point to `app.html`.

## Login IDs and passwords (DEMO ONLY)

| Role | ID | Password |
|---|---|---|
| Super Admin | owner@tomato.demo | OwnerDemo2026! |
| Manager | manager@tomato.demo | ManagerDemo2026! |
| Staff | staff@tomato.demo | StaffDemo2026! |
| Customer | customer@tomato.demo | CustomerDemo2026! |

Sign out to change roles. Demo signup is a **preview, not a real account**. No backend, payment or real user access is activated by this demo.

## Real authentication

This fixed one-file demo intentionally starts unconfigured, so it works on GitHub Pages even if `config.js` and `app.js` were omitted in your upload. To use real Supabase authentication, first configure the deployment architecture appropriately, run the reviewed SQL scripts in `supabase/`, and verify RLS in the connected project. Never publish service-role keys. The standalone demo passwords are public test data and are not secure authentication. See the complete original architecture notes if you need to deploy live accounts.

## Verification

The fixed `app.html` contains no external application JavaScript or CSS dependencies. Google Fonts are an optional cosmetic dependency; core login and demos work without them. Product photographs are embedded for the demo; storefront images use `assets/`.

### Alternative URL if your old `app.html` is cached

`roles.html` is the **same complete working demo** with a new filename. Upload `roles.html` to the repository root and open `https://YOUR-USERNAME.github.io/YOUR-REPO/roles.html` to bypass a cached broken `app.html`. The store navigation will still use `app.html`, so upload the fixed `app.html` as well for permanent repair.
