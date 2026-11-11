# Prospective-student resource finder

Prepared before implementation, 2026-11-11.

Student/group: not supplied; student should add name before submission.
Audience: prospective student (explicitly selected by the student in chat).
Visitor task: find a relevant Alvernia location, distinguish its type, and open its source before planning a visit.
Observed problem: source inspection shows category filters but no location-type filter; an unmatched query only suggests another search or adding a resource. On phones the map appears before the directory. These are agent observations, not peer findings.
Evidence: original index.html finder section and app.js renderPlaces; before screenshots captured from unmodified starter.
Improvement: add location-type filtering, a visible result summary and full reset, with directory and selected details before the optional map on phones.
Why it matters: prospective students can avoid confusing a planned or partner location with a campus and recover without editing data.
Path: resource finder.

## Scope and boundaries
Edit index.html, style.css, app.js, core.js, test-core.js and submission documentation. Preserve all existing records, source dates, map controls, WebGL fallback, resource editing/export/import, video controls, concept labels, and media credits. No new university facts, services, APIs, tokens, or 3D work. Existing dated records remain attributed to the starter and require confirmation before visiting.

## Three acceptance criteria
1. Choosing Campus shows only the three campus seed records; searching Reading within that type shows two results. Selecting a result exposes its address, unknown-access note and source link without loading a map.
2. At 390px width, directory and detail appear before the optional map; keyboard users can select a type, reach a result and its details with visible focus, and use Reset.
3. Searching zzz-no-match shows zero matches, hides stale location details, and offers Reset all filters. Reset restores all seven seed places, clears the search and type/category filters, and focuses search.

## Workflow and student judgment
Student chose prospective-student resource finder over other audiences. Agent proposed location-type filtering and empty-search recovery and implements this bounded scope. Implementation choices below are agent recommendations until the student reviews them.
Agent decision: preserve the existing map but prioritize directory information on phones because visiting details should not depend on WebGL.
Student change/rejection of an AI suggestion: pending authentic student review; do not claim the agent decision as the student's.

## Evidence and completion
Run existing core tests plus type/filter regression checks. Capture before/after desktop and phone images. Append dated outcomes to TEST_LOG.md; separate passed, failed and untested. Peer observation, resulting revision/retest and the student's 60–90 second demonstration remain pending. No Canvas due date was provided; use the date shown in Canvas.

Student review: explicitly selected “Keep details first on phones.”
