# Verification log

## Starter verification · 2026-10-30

- JavaScript syntax checks: passed for app.js, map.js, core.js.
- Automated validation: 10 test groups passed (run `node test-core.js`).
- Desktop browser: landing page/official background video rendered; carousel added a fourth YouTube slide; lookalike YouTube domain rejected; temporary test slide removed.
- Resource UI: sourced QA record saved, progress changed to 1/5, survived page reload, found by search, and removed. Export displayed the successful data-export message. Test data was removed from the preview.
- Mobile CSS: inspected in a 390-pixel iframe; hero, navigation, resource search, and map layout fit. DOM measured no horizontal overflow (375-pixel content width, 375-pixel scroll width).
- Cesium and model-viewer: browser cannot initialize WebGL 2. Clear fallback is included; actual 3D rendering, tile coverage, and model placement are not verified here.
- No user Cesium token was supplied. Real-token authentication, Google asset entitlement/quota, and live photorealistic tiles still require a check on an authorized WebGL-enabled device.
- A video URL’s syntax can be tested without verifying whether its owner allows playback. Test your chosen YouTube video after adding it.
- GLB file structure and local asset references checked separately during packaging.
- Imported JSON validation is automated; browser file-picker import/upload paths still need a student-device check.

## Student test record

| Scenario | Expected | Observed | Pass/fix/untested |
| --- | --- | --- | --- |
| Add five distinct resources | Five new pins; sources retained; 5/5 | | |
| Same resource twice | No inflated count | | |
| Search with no result | Clear empty state | | |
| Invalid video URL | Rejected without embedding | | |
| My actual YouTube story | Plays or useful external link | | |
| Export and import | Data survives; no token in JSON | | |
| Real token + tiles | Photorealistic scene or clear account/coverage error | | |
| My GLB on campus | Correct size, heading, ground contact | | |
| Keyboard + phone | Navigation and forms usable | | |
| Wrong or missing evidence | Claim corrected or left unknown | | |


## This week's redesign — student evidence
Complete this section for the chosen page/feature. The earlier map/GLB rows are
optional unless those features are part of the chosen redesign. Do not mark
the starter's historical results as results of your own work.

| Check | Expected | Observed | Pass / fix / untested |
| --- | --- | --- | --- |
| My acceptance test 1 | | | |
| My acceptance test 2 | | | |
| My acceptance test 3 | | | |
| Phone-width layout | | | |
| Keyboard path and visible focus | | | |
| Empty, invalid, or unavailable state | | | |
| Peer completes the assigned task | | | |
| Revised feature retest | | | |
| Published page and relative links | | | |
| Existing node test-core.js (if available) | | | |

Peer's task and observed difficulty:
What I changed after the peer test:
Known limitation and next step:

## Resource-finder redesign · 2026-11-11 · agent run

Passed: node test-core.js — all 10 original groups plus 8 new assertions for campus/partner/planned/student types, combined search/category filters, empty results and reset inputs. app.js syntax check passed.

Source-link check: official Reading locations, Post Center and Contact Us pages returned content through the web tool. This checks those three destinations; it is not a fresh audit of all source records. Other outbound destinations not reverified.

Browser infrastructure failed: Playwright's bundled browser was missing, Edge could not launch successfully, and installed Chrome could not reach localhost (network denied, then timed out even after permission and server restart). Automated browser assertions therefore are NOT reported as passed. Screenshot capture was attempted but not verified.

AC1: filtering logic passed in Node; browser interaction unverified. AC2: phone layout/keyboard unverified. AC3: empty-match logic passed in Node; visible recovery and focus unverified. Browser test procedure is supplied in submission guide.

Peer test: untested, requires another person. Peer-driven revision/retest: pending. Real-token tiles, WebGL/model rendering, new resource UI, export/import UI and hosted relative links: untested in this run. Original historical results above are not current-run results.

Implementation review revision: location-type reset was added to existing All locations, featured-campus and save-resource flows so a prior type filter cannot hide their target. Syntax and regression tests will be rerun after this change. This is agent review, not peer evidence.

### Browser follow-up — file-origin checks succeeded
After correcting the file preview to index.html (not a directory), the automated Chrome run passed all three acceptance checks. AC1: Campus = 3; Reading + Campus = 2; Enter on a result focuses details, including source and unknown-access text. AC2: 390px viewport and scroll width both 390px; details/results precede map; Tab from type selector reaches Reset; Enter resets and focuses search. AC3: unmatched Partner search gives zero buttons, hides stale details, and empty-state Reset restores seven places and clears type/query. Screenshots were generated and after desktop/phone/details images visually inspected. Visible search focus ring confirmed in phone screenshot.

These are local file-origin directory tests, not HTTP hosting or live map verification. HTTP preview remains blocked. Before/after desktop/phone and empty-state PNGs are in the evidence folder. The earlier infrastructure failures remain recorded for provenance and are superseded only for these directory checks. Final core/syntax rerun passed unchanged.

Publication: site registration succeeded, but source publishing did not complete. First helper attempt failed with “Unable to start Git”; a retry with bundled Git on PATH produced no completion and was stopped. No live URL or pushed repository is claimed. ZIP requires instructor approval before use as fallback.
Final helper output requested renewing the source credential before retrying. Publication remains incomplete; no deployment URL was returned.
