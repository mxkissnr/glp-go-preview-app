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
