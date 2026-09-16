# Error log

## 2026-08-12 — Stitching full-page Shopify captures

- **What did not work:** Chrome's full-page capture returned no image data. The first stitching attempt also failed because Sharp was imported from the wrong runtime, and the next used device-pixel-ratio assumptions that produced invalid crop bounds.
- **What worked instead:** Captured overlapping viewport segments, loaded the bundled Sharp runtime, derived crop dimensions from each bitmap's actual metadata, and stitched those exact regions.
- **Note for next time:** Chrome screenshots may be CSS-pixel bitmaps even when the page reports `devicePixelRatio: 2`; calculate crops from image metadata, not DPR.

## 2026-08-31 — Playwright verification of a local HTML copy

- **What did not work:** The sandboxed Playwright wrapper could not reach npm; Playwright blocked direct `file:` navigation; serving all of `/private/tmp` was rejected because it exposed unrelated temporary data.
- **What worked instead:** Downloaded the CLI with explicit approval, copied the review file into the dedicated project `output/playwright/` folder, and served only that folder over localhost.
- **Note for next time:** For local HTML review, begin with a dedicated review directory and localhost server. Do not serve broad temporary directories or depend on `file:` navigation.

## 2026-09-16 — Porting the globe animation into the Bandung deck (slide 5)

- **What did not work:** Loading the whole 2MB NextGen deck in an iframe and faking arrow-key presses into it rendered black: the injected CSS raced the iframe load and cross-document key events were unreliable. First native port dropped `parseHash` when replacing the script block (ReferenceError on load). Second attempt left `left:var(--h-x)` on the globe bodies while JS positioned them via `translate3d`, so the globe sat off-frame bottom-right. Verifying in the in-app Browser pane also failed because a hidden pane pauses `requestAnimationFrame`, so the animation never advanced.
- **What worked instead:** Inlined the globe markup, CSS, and progress-driven JS directly into the deck; removed the CSS `left/top` vars so `translate3d` is the sole positioning source; verified with Playwright driving installed Chrome (`chromium.launch({channel:'chrome'})`, cached npx playwright at `~/.npm/_npx/31e32ef8478fbf80`) against the localhost server.
- **Note for next time:** Never verify rAF-driven animation through a hidden Browser pane. Use Playwright + Chrome channel. When replacing a script region by start/end markers, grep for every function defined inside the range first.
