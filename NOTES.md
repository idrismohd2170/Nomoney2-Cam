# Project notes

## Context
- Working name: Nomoney2-Cam (the repository name). A distinct product name and brand are required before any public release.
- The repository is empty: no files, commits, branch contents, stack, or GitHub Actions runs exist yet.
- The target is an Android camera experience informed by its public Play listing and the user-supplied technical summary. Rebuild feature concepts only; do not place the original app name, branding, copy, assets, or proprietary filter data in this repository.
- Because the repository is empty and the requested glass library is browser-based, the app will use a web UI wrapped with Capacitor for Android.

## Done
- Inspected the GitHub repository and confirmed it has no existing stack or CI to preserve.
- Read the public Play listing and the liquid-glass-js README; checked the official Ponytail full-mode instructions.
- ✅ Inspected the empty repository and recorded the initial stack and scope decisions.

## Next steps (ordered)
1. Write `docs/recon.md`, classifying feature candidates as must, should, or could from the public listing and screenshots; use the supplied technical summary only as a high-level cross-check. Install the official Ponytail project instructions before app code.
2. Scaffold the web app and Capacitor Android project, then verify a local/CI build.
3. Add the push-triggered debug-APK GitHub Actions workflow (JDK 17, Node LTS, web build, Capacitor sync, Gradle assembleDebug, artifact upload; no signing or secrets) and verify the run.
4. Add camera preview and photo capture.
5. Add the app shell with liquid-glass controls, following the library README API exactly.
6. Implement each must-have from `docs/recon.md` in its own pushed commit, rewriting this file after every step.

## Could be better
- There is no app scaffold, build setup, test harness, or CI; all must be introduced within the requested steps.
- No Actions run can be checked until the workflow exists in step 3.

## Decisions
- Use a web UI plus Capacitor Android because the repository is empty and liquid-glass-js is a browser library.
- Use only the repository name as a temporary working name; choose fresh branding before public release.
- Keep all implementation original: no reference-app name, copy, logo, icon, image, filter/LUT data, or other original asset.
- Apply Ponytail at full level for all code. Its official instructions have been read; the project-level instruction file will be added before any app implementation.
- Do not add dependencies beyond Capacitor and requirements documented for liquid-glass-js without asking.

## Open questions
- Final product name and branding remain open; they must be decided before any public release.
- No decisions block steps 2–4.
