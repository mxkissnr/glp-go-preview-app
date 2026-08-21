# GLP Go Preview — not for end users

This repository exists so the GLP maintainer can test the **Go rewrite** of
the backend on a real Home Assistant instance, ahead of it ever becoming the
shipping implementation. It ships no source code: it is a Home Assistant app
manifest that points at a container image built from `go/Dockerfile` on the
`go-migration` branch of
[gaggiuino-local-profiler](https://github.com/mxkissnr/gaggiuino-local-profiler).

**If you are looking for GLP, you want the stable app instead:**
<https://github.com/mxkissnr/gaggiuino-local-profiler>

## What "Go rewrite" means here

The stable app and the Node dev channel (`glp-dev-app`) both run the
original Express/Node backend (`server.js`, `lib/`, `routes/`). This channel
runs a from-scratch reimplementation of that same backend and frontend in Go
(`gaggiuino-local-profiler/go/` in the main repo) — a single static binary,
no Node/npm, no native addons, `modernc.org/sqlite` instead of
`better-sqlite3`. It targets the same `openapi.yaml` contract and opens the
same `/data/glp.db` schema, but it is a **separate, independent
implementation under active development**, not a build of the Node code.

## What you get if you install this anyway

Unreleased, experimental code, from a rewrite that has not yet been proven
in real-world use. Whole feature areas may be incomplete or behave
differently from the Node app — see the main repo's `go/README.md` for the
exact current phase and scope. It is expected to be broken at times, may
corrupt its own database, and carries no upgrade path — the stable app will
not import anything from it, and neither will the Node dev channel. There
are no release notes beyond the auto-generated commit log below and no
support for this channel.

## How it coexists with the stable app and the Node dev channel

The Go preview app uses its own slug (`glp_go_preview`), so Home Assistant
treats it as a completely separate app from both the stable app
(`gaggiuino_local_profiler`) and the Node dev channel
(`gaggiuino_local_profiler_dev`):

| | Stable | Node dev | Go preview |
|---|---|---|---|
| Slug | `gaggiuino_local_profiler` | `gaggiuino_local_profiler_dev` | `glp_go_preview` |
| Backend | Node/Express | Node/Express | Go |
| Data directory | its own `/data` | its own `/data` | its own `/data` |
| Web port | 8099 | 8098 | 8097 |
| Sidebar | GLP | GLP DEV | GLP Go |

Separate slugs mean separate persistent storage, so this channel can never
write to the stable app's or the Node dev channel's shot archive or coffee
library. All three can run at the same time. Point them at the same machine
only if you accept that all installed channels will sync shots from it.

Go preview builds are published for **amd64, armv7 and aarch64** — same
architecture coverage as the stable app and the Node dev channel.

## Maintainer setup

1. Home Assistant → Settings → Apps → Store → ⋮ → Repositories
2. Add `https://github.com/mxkissnr/glp-go-preview-app`
3. Install **GLP Go**

Each push to `go-migration` in the main repository builds a new image and
bumps `version` in this repository's `config.yaml`, which is what makes Home
Assistant offer the update. See
`.github/workflows/go-preview-publish.yaml` in the main repository.

**This channel is not live yet** — `go-preview-publish.yaml` needs a repo
secret (`GO_PREVIEW_ADDON_REPO_TOKEN`) on the main repository before its
first run can push a commit here. See that workflow's own header comment,
and `go/README.md`'s "Go preview channel (publishing)" section in the main
repository, for exactly what's still needed.
