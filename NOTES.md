# Project notes

## Context
- Working name: Nomoney2-Cam (the repository name). A distinct product name and brand are required before any public release.
- The repository started empty; it now has a main branch and this project plan. No existing app stack or workflow was present.
- The Android camera experience is guided by public listing features and the high-level user-supplied summary. The repository must not contain original branding, copy, assets, or proprietary filter data.
- The selected stack is a web UI wrapped with Capacitor for Android because the repository was empty and liquid-glass-js is browser-based.

## Done
- Inspected the empty repository; created initial NOTES.md and pushed commit 3c109e3da90695967761dca8ce542eb87d41c104.
- Wrote docs/recon.md from the public listing/review information and installed the upstream Ponytail project instructions.
- ✅ Classified the feature scope and installed Ponytail before app implementation.

## Next steps (ordered)
1. Scaffold the web app and Capacitor Android project; verify it builds.
2. Add the push-triggered debug-APK GitHub Actions workflow (JDK 17, Node LTS, web build, Capacitor sync, Gradle assembleDebug, artifact upload; no signing or secrets) and verify the run with gh run watch.
3. Add live camera preview, still capture, and local save.
4. Add the app shell with liquid-glass controls, following the library README API exactly.
5. Implement the must-have original analog-look treatment in one commit.
6. Implement the must-have two-exposure double exposure in one commit.
7. Reassess remaining should/could items from docs/recon.md without expanding scope or adding unapproved dependencies.

## Could be better
- The public listing extraction exposed review text but not the screenshot image contents, so visual layout details still need direct inspection before UI styling.
- Public reviews mention camera startup and look-availability reliability issues; local persistence and graceful camera errors should be verified during implementation.
- Purchase pricing, restore semantics, and exact catalog behavior are unspecified and remain out of scope for real billing.
- No workflow run exists yet; CI evidence becomes available only after the workflow is added.

## Decisions
- Use a web UI plus Capacitor Android; no existing stack existed.
- Use only the repository name as a temporary working name; rebrand before any public release.
- Keep the implementation original: no target app name, copy, branding, icons, images, filter/LUT data, model files, or other original assets.
- Apply Ponytail at full level for all code. Its official instructions are installed in AGENTS.md from https://github.com/DietrichGebert/ponytail (MIT).
- Use liquid-glass-js according to its README; do not guess its API.
- Do not add dependencies beyond Capacitor and documented liquid-glass-js requirements without asking.
- No live payments, paid service, signing key, or secret is in scope.

## Open questions
- Final product name and branding are open; decide before any public release.
- No decision blocks scaffolding or CI.
