# Feature reconnaissance

## Evidence and limits
- Source: the public Google Play listing and its public review section, read on 2026-10-19. The listing's screenshot links were visible, but this page extraction did not expose screenshot image details; no visual-layout assumptions are claimed here.
- The user-supplied technical summary is a supplementary, high-level hint only. This list does not reproduce original implementation details, names, assets, copy, or filter data.
- Priority means importance to a small independent camera app, not a claim about the reference app's internal architecture.

## Must
- **Live preview, capture, and save** — the requested Android camera flow must open a live camera view, capture a still, and preserve the result locally.
- **Original analog-look treatment** — after capture, apply an independently authored look with a randomized analog-style treatment. The listing describes tone curves, grain, dust, light leaks, vignette, sharpening, and frames; recreate these effects with original parameters and graphics, not copied LUTs or assets.
- **Double exposure** — let the user take two exposures and combine them into one image.

## Should
- **Camera/look selection** — let users choose among original looks, and structure the UI so additional looks can be added later.
- **Camera catalog and unlock state** — the listing describes cameras that can be obtained and used, with a membership unlocking a larger catalog and exclusive options. Build a non-payment catalog/unlock experience only if it fits the allowed scope; do not add real billing or a paid service without approval.
- **Import an existing photo** — described as a membership tool; make imported-photo processing an optional follow-up, not a dependency of taking pictures.
- **Development delay controls** — the listing describes a development wait and a membership option to disable it. If implemented, keep it transparent and non-blocking; no network dependency is required.
- **Reliability around looks and camera startup** — public reviews report intermittent camera-opening and missing-look/download issues. Keep the capture path resilient and avoid making locally available looks disappear when offline.

## Could
- **Face-aware retouching or background effects** — mentioned only in the user-supplied technical summary, not the public listing text reviewed here; defer unless the core camera experience is complete and a clean, original implementation is feasible.

## Build order for must-haves
1. Live preview, capture, and local save — covered by the camera step.
2. Original analog-look treatment — one dedicated feature commit.
3. Two-exposure double exposure — one dedicated feature commit.

## Excluded from this scope
- No original app name, package identifier, branding, icons, photographs, text, LUT/filter files, model files, or other original assets.
- No decompilation, APK download, copied proprietary implementation, account/login SDKs, analytics, push SDKs, or real payment integration.
- No feature beyond the listed priorities unless the user asks.
