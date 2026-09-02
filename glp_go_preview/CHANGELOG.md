## go-preview-20260902_1909 — 2026-09-02

- feat(go): persistent GaggiMate live client, stop the per-tick WS hammer (#952) (29793ba)
- feat(go): port the automatic shot-sync triggers (#953) (92c1c2e)
- fix(go): coalesce buffered live-snapshot SSE frames on a slow consumer (#901) (6052714)
- perf(go): fold grinder wear in one shot scan for GET /api/library (#951) (240356a)
- perf(go): pool warm resvg contexts for the share card (#951) (58bd8c6)
- perf(go): keep /shots.json datapoints raw + goccy encoder (#951) (54e7a01)

## go-preview-20260902_1249 — 2026-09-02

- fix(go): accept URL-safe HA ingress tokens in the path-prefix verdict (#901) (ff23165)

## go-preview-20260902_1230 — 2026-09-02

- feat(go): add an HA-ingress self-diagnostic to internal/debug (#901) (5d4c5d6)

## go-preview-20260902_1154 — 2026-09-02

- refactor(go): extract buildApp + add an HA-ingress smoke test (#901) (af85e68)
- test(go): Node-vs-Go route-parity check, wired into CI (#901) (1f92bdd)
- test(go): extend Phase-2 contract-test coverage (#901) (2b2da64)

## go-preview-20260902_1116 — 2026-09-02

- feat(go): port the debug routes (#901) (2cd65b0)
- feat(go): port the share-card PNG renderer (#901) (2392282)

## go-preview-20260902_0819 — 2026-09-02

- feat(go): port the MQTT live-data transport (#901) (96d229b)
- feat(go): port the bean-import domain (#901) (f71e0cd)

## go-preview-20260902_0746 — 2026-09-02

- feat(go): port the achievements ("stamp card") domain (#901) (4a20791)
- feat(go): port geocodeBean + the trivial system/machine-control routes (#901) (3757898)

## go-preview-20260902_0658 — 2026-09-02

- build(go): add frontend build stage to the Docker image and Makefile (#901) (01c5bcf)
- feat(go): serve the Vite SPA from the binary, move templ pages under /ui/ (#901) (721491a)

## go-preview-20260902_0636 — 2026-09-02

- feat(go): port BREW_AUTO auto-stop, live idle stats + steam/flush states, milk restock (#901) (d9eb10f)

## go-preview-20260825_1111 — 2026-08-25

- fix(go): deterministic tiebreak for comparative grind-advice bucket selection (#901) (3b0a488)
- fix(go): wire orders-update SSE publish onto the REST API's Service instance too (#901) (6d8de01)
- fix(go): reject null in boiler settings numeric fields (#901) (e0c06df)

## go-preview-20260825_0738 — 2026-08-25

- docs(go): update README Status/Frontend sections for this round's four packages (#901) (fd9f7d3)
- feat(go): A/B compare mode, ghost-curve overlay, score-delta chip, comparative grind-advice panel on shot detail (#901) (64a9d0e)
- feat(go): port calcComparativeGrindAdvice as internal/shots.ComputeComparativeGrindAdvice (#901) (6dfe07b)

## go-preview-20260825_0721 — 2026-08-25

- feat(go): real SSE live-update for the Orders queue, replacing 10s polling (#901) (15fecf2)

## go-preview-20260825_0713 — 2026-08-25

- feat(go): make boiler/system Settings editable with real field-level validation (#901) (3a96082)
- feat(go): freshness/firmware/ordered-by badges on the Shots list (#901) (fdacd83)

## go-preview-20260825_0700 — 2026-08-25

- feat(go): full Edit UI for Library and Machines pages (#901) (dbaa06f)
- refactor(go): extract library/machine PUT handlers into exported update.go service functions (#901) (54822b9)

## go-preview-20260822_0749 — 2026-08-22

- feat(go): Shots master-detail view with metrics, verdict, and chart (6bc68bb)
- fix(go): correct dangling README cross-reference in layout.templ (9a0bb7a)
- feat(go): fixed left icon sidebar replaces the top-tab menu (e383dd2)

## go-preview-20260821_1025 — 2026-08-21

- fix(go): correct README's stale Library/Settings "read-only" claims (#901) (ee08d44)
- feat(go): verdict-first default-machine status on the Machines page (#901) (5b0f644)
- feat(go): verdict-first due/soon/ok summary on the Maintenance page (#901) (f8a0ef9)
- feat(go): stock bars for Beans/Milks on the Library pages (#901) (8b0dd20)

## go-preview-20260821_0843 — 2026-08-21

- fix(go): restore styled htmx error fragments with a generic class (38d17bf)
- feat(go): Verdict header for Shots list + read-only tone for Settings (#901) (532a855)

## go-preview-20260821_0829 — 2026-08-21

- feat(go): port Instrument design-token system onto templ frontend (#901) (740ae98)

## go-preview-20260821_0752 — 2026-08-21

- fix(go): address code-review findings on Settings/Library/Machines forms (#901) (0bd9aad)
- feat(go): Create/Edit forms for Library, Machines, and all 5 Settings categories (#901) (35afcbc)
- fix(go): raise GET /api/token rate limit for genuine Ingress callers (#901) (fda1212)

## go-preview-20260821_0652 — 2026-08-21

- fix(go): X-Frame-Options DENY -> SAMEORIGIN, blocked HA sidebar panel embed (02affd9)

## go-preview-20260821_0640 — 2026-08-21

- fix(go): make every template href/src/hx-* path Ingress-safe (#901) (290dcfe)

## go-preview-20260821_0624 — 2026-08-21

- fix(go): register GET / so HA Ingress's base URL stops 404ing (38d8aaa)

## go-preview-20260821_0609 — 2026-08-21

- fix(go): wire GLP_DEV_BUILD through the go-preview image build (#901) (cbe833e)

# GLP Go Preview changelog

Populated automatically by `.github/workflows/go-preview-publish.yaml` in
the main repository on every push to `go-migration`. Not maintained by hand.
