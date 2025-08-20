
# Hill AFB Visit Tracker

Installable, offline web app for tracking customer visits (R/Y/G status, frequency-based due dates).

## Deploy (Azure Static Web Apps — Fast)

1. Create a GitHub repo (public or private), e.g., `hill-afb-visit-tracker`.
2. Upload these files to the repo root and commit.
3. In **Azure Portal** → **Static Web Apps** → **Create**:
   - Deployment source: **GitHub**
   - Repository/Branch: choose your repo & `main`
   - Build preset: **No framework**
   - App location: `/`
   - API location: *(leave blank)*
   - Output location: *(leave blank)*
   - Create.
4. When the URL is ready, open it in **Safari** → Share → **Add to Home Screen**.

## Deploy (GitHub Pages)

1. Repo **Settings → Pages** → Source: **Deploy from a branch**; Branch: `main`; Folder: `/root`.
2. Open the Pages URL in Safari → **Add to Home Screen**.

## Updating the app (force-refresh)

- Edit `sw.js` and bump `CACHE_NAME` (e.g., `visit-tracker-v3 → visit-tracker-v4`) and commit.
- Users: open the app, then quit/relaunch once to load the new cache.

## Backup/Restore

- Use **Export** in the app to save `visit-tracker-backup.json` to OneDrive.
- On a new device: **Import JSON** in the app and select that file.
