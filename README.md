 # Crypto Max V10 — Android project

Crypto Max is an offline-first personal organizer for tracking free crypto-reward opportunities. It is **not** a wallet, exchange, automatic airdrop claimer, or source of guaranteed income.

## Features
- Professional dark interface with integrated CM / Crypto Max brand mark and Android launcher icon.
- Rewards tracker: add, edit, filter, search, status, notes, optional official link, and user-entered USD estimate.
- Opportunity checklist focused on official sources, no-deposit rules, withdrawal terms, and wallet safety.
- Manual market reference notes (not live prices or trading signals).
- Local JSON backup export; records are stored on this device in WebView local storage.
- No account, analytics SDK, wallet connection, seed-phrase input, or external JavaScript libraries.
- GitHub Actions workflow builds and uploads `app-debug.apk` as the `Crypto-Max-V10-APK` artifact.

## Build APK in GitHub
1. Upload the **contents** of this project folder to the root of your GitHub repository (including the `.github` folder; enable showing hidden files if needed).
2. Open **Actions** → **Build Crypto Max V10 APK**.
3. Press **Run workflow** (or push to `main` / `master`). Wait for all steps to pass.
4. Open the completed workflow run and find **Artifacts** → `Crypto-Max-V10-APK`.
5. Download the artifact ZIP, extract it, and install `app-debug.apk` on Android. You may need to allow installs from that download source.

## Build locally
Requires JDK 17, Android SDK platform 35, build-tools 35.0.0, and Gradle 8.9:

```bash
gradle --no-daemon :app:assembleDebug
```

APK output: `app/build/outputs/apk/debug/app-debug.apk`.

## Important limitations
- Reward records and manual prices are user-entered and are not independently verified.
- Sample data is intentionally zero by default; no fake balance or earnings are shown.
- No automatic rewards collection, wallet signing, trading, or push notifications are implemented.
- This project does not include a release signing key. The debug APK is for personal testing; do not publish it as a production release.
