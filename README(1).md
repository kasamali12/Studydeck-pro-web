# StudyDeck Pro website

Static site, no build step.

## Upload these files to GitHub (same folder, repository root)
- `index.html` (required) the whole website. The Android app is built into it, so the "Download APK" button works by itself.
- `icon-512.png` (required) logo, favicon and home-screen icon
- `studydeck-v1_0_0.apk` (recommended) the plain file, used by the "Copy link" button so people can share a direct link
- `.nojekyll` (recommended) empty file so GitHub Pages serves everything as it is
- `README.md` (optional)

## Publish on GitHub Pages
1. Create a repository and upload the files above.
2. Settings, Pages, Source: "Deploy from a branch", Branch `main`, folder `/ (root)`.
3. The site opens at `https://<username>.github.io/<repo>/`.

## Ship a new app version
1. Upload the new APK. Get its checksum with `sha256sum yourfile.apk`.
2. In `index.html` update `APK_URL`, the `SHA` value, the version and size line, and replace the base64 text inside `<script id="apkdata">` (`base64 -w0 yourfile.apk`).
