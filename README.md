# jeeman-releases

Public **installer binaries only** for Jeeman in-app updates.

- Desktop: `Jeeman-POS-Setup-<version>.exe`
- Mobile: `Jeeman-<version>.apk` (or `Jeeman.apk`)

**No application source code** belongs in this repository. Source stays in private repos (`Jeeman`, `Jeeman-mobile`).

## How updates work

1. Build installers locally.
2. Create a [GitHub Release](https://github.com/HiteshKumar777/jeeman-releases/releases) tagged like `v1.0.2`.
3. Attach the `.exe` and `.apk`.
4. Copy each asset download URL into Firebase Firestore `appConfig/releases` (`desktop.url` / `android.url`).
5. Optionally set `desktop.sha256` / `android.sha256` (SHA-256 of each file) for integrity checks.
6. Keep only **current + previous** release assets to avoid clutter.

License / activation still gates who can run the POS — this repo only hosts downloadable installers.
