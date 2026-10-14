# OWNCAST

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-movies_media-lightgrey)

> Anticloud-hardened packaging of the upstream project `OWNCAST` in category **MOVIES MEDIA**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** MOVIES MEDIA · **Upstream:** https://github.com/owncast/owncast · **Upstream pin:** `cd64bdf44f11998e71e6c4e9ac522ea4a8f2dd1a` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

<p align="center">
  <a href="https://github.com/owncast/owncast" alt="Owncast">
    <img src="https://owncast.online/images/logo.png" alt="Owncast Logo" width="200">
  </a>
</p>

<p align="center">
	<strong>Take control over your content and stream it yourself.</strong>
</p>

<br/>

<p align="center">
	<a href="https://github.com/owncast/owncast/blob/develop/LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License" />
  </a>
</p>

<br/>

<p align="center">
	<a href="https://owncast.online"><strong>Explore the docs »</strong></a>
	<br />
	<a href="https://watch.owncast.online/">View Demo</a>
	·
	<a href="https://owncast.online/faq/">FAQ</a>
	·
	<a href="https://github.com/owncast/owncast/issues">Report Bug</a>
	·
	<a href="docs/SECURITY.md">Report Security Issue</a>
</p>

<!-- TABLE OF CONTENTS -->

## Table of Contents

- 📒 [About the Project](#about-the-project)
- 🚀 [Getting Started](#getting-started)
- 👨‍💻 [Use with your broadcasting software](#use-with-your-existing-broadcasting-software)
- 🛠 [Building from source](#building-from-source)
  - 🚨 [Important note about source code and the develop branch](#important-note-about-source-code-and-the-develop-branch)
  - 🗄️ [Backend](#backend)
  - ⚛️ [Frontend](#frontend)
- 👏 [Contributing](#contributing)
  - 💵 [Donors](#donors)
- [Security](#security)
- 📝 [License](#license)
- [Contact](#contact)

<!-- ABOUT THE PROJECT -->

## About The Project

<p align="center">
  <a href="https://owncast.online/images/owncast-splash.png">
    <img src="https://owncast.online/images/owncast-splash.png" width="70%">
  </a>
</p>

Owncast is an open source, self-hosted, decentralized, single user live video streaming and chat server for running your own live streams similar in style to the large mainstream options. It offers complete ownership over your content, interface, moderation and audience. <a href="https://watch.owncast.online">Visit the demo</a> for an example.

<div>
    <img alt="GitHub all releases" src="https://img.shields.io/github/downloads/owncast/owncast/total?style=for-the-badge">
	  <a href="https://hub.docker.com/r/owncast/owncast">
      <img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/owncast/owncast?style=for-the-badge">
	  </a>
    <a href="https://github.com/owncast/owncast/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22">
      <img alt="GitHub issues by-label" src="https://img.shields.io/github/issues-raw/owncast/owncast/good%20first%20issue?style=for-the-badge">
    </a>
    <a href="https://opencollective.com/owncast">
      <img alt="Open Collective backers and sponsors" src="https://img.shields.io/opencollective/all/owncast?style=for-the-badge">
    </a>
</div>

---

<!-- GETTING STARTED -->

## Getting Started

The goal is to have a single service that you can run and it works out of the box. **Visit the [Quickstart](https://owncast.online/docs/quickstart/) to get up and running.**

## Use with your existing broadcasting software

In general, Owncast is compatible with any software that uses `RTMP` to broadcast to a remote server. `RTMP` is what all the major live streaming services use, so if you’re currently using one of those it’s likely that you can point your existing software at your Owncast instance instead.

OBS, Streamlabs, Restream and many others have been used with Owncast. [Read more about compatibility with existing software](https://owncast.online/docs/broadcasting/).

## Building from Source

Owncast consists of two projects.

1. The Owncast backend is written in Go.
1. The frontend is written in React.

[Read more about running from source](https://owncast.online/development/).

### Important note about source code and the develop branch

The `develop` branch is always the most up-to-date state of development and this may not be what you always want. If you want to run the latest released stable version, check out the tag related to that release. For example, if you'd only like the source prior to the v0.1.0 development cycle you can check out the `v0.0.13` tag.

> Note: Currently Owncast does not natively support Windows servers. However, Windows Users can use Windows Subsystem for Linux (WSL2) to install Owncast. For details visit [this document](https://github.com/owncast/owncast/blob/develop/contrib/owncast_for_windows.md).

### Backend

The Owncast backend is a service written in Go.

1. Ensure you have prerequisites installed.
   - C compiler, such as [GCC compiler](https://gcc.gnu.org/install/download.html) or a [Musl-compatible compiler](https://musl.libc.org/)
   - [ffmpeg](https://ffmpeg.org/download.html)
1. Install the [Go toolchain](https://golang.org/dl/) (1.24 or above).
1. source the project. `git source https://github.com/owncast/owncast`
1. `go run main.go` will run from the source.
1. Visit `http://yourserver:8080` to access the web interface or `http://yourserver:8080/admin` to access the admin.
1. Point your [broadcasting software](https://owncast.online/docs/broadcasting/) at your new server and start streaming.

### Frontend

The frontend is the web interface that includes the player, chat, embed components, and other UI.

1. This project lives in the `web` directory.
1. Run `npm install` to install the Javascript dependencies.
1. Run `npm run dev`

## Contributing

Owncast is a growing open source project that is giving freedom, flexibility and fun to live streamers.
And while we have a small team of kind, talented and thoughtful volunteers, we have gaps in our skillset that we’d love to fill so we can get even better at building tools that make a difference for people.

We abide by our [Code of Conduct](https://owncast.online/contribute/) and feel strongly about open, appreciative, and empathetic people joining us.
We’ve been very lucky to have this so far, so maybe you can help us with your skills and passion, too!

If you're new to the project, maybe you'd be interested in looking at [![Good First Issue](https://img.shields.io/gi

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Go** (manifests: go.mod, go.sum; scanned in UPSTREAM_CLONE)
- Top-level source layout: `auth/`, `build/`, `config/`, `contrib/`, `db/`, `logging/`, `metrics/`, `models/`, `notifications/`, `persistence/`, `pluginhost/`, `services/`
- Snapshot size: **1662 files**, **102355 lines of code** (measured; see Benchmarks)
- Primary languages: `.js` (613), `.go` (381), `.tsx` (164), `.svg` (109), `.woff2` (55), `.woff` (52)
- Upstream commit pinned for this packaging: `cd64bdf44f11998e71e6c4e9ac522ea4a8f2dd1a`

---

## Installation

- 👨‍💻 [Use with your broadcasting software](#use-with-your-existing-broadcasting-software)
- 🛠 [Building from source](#building-from-source)
  - 🚨 [Important note about source code and the develop branch](#important-note-about-source-code-and-the-develop-branch)
  - 🗄️ [Backend](#backend)
  - ⚛️ [Frontend](#frontend)
- 👏 [Contributing](#contributing)
  - 💵 [Donors](#donors)
- [Security](#security)
- 📝 [License](#license)
- [Contact](#contact)

<!-- ABOUT THE PROJECT -->

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

- 👨‍💻 [Use with your broadcasting software](#use-with-your-existing-broadcasting-software)
- 🛠 [Building from source](#building-from-source)
  - 🚨 [Important note about source code and the develop branch](#important-note-about-source-code-and-the-develop-branch)
  - 🗄️ [Backend](#backend)
  - ⚛️ [Frontend](#frontend)
- 👏 [Contributing](#contributing)
  - 💵 [Donors](#donors)
- [Security](#security)
- 📝 [License](#license)
- [Contact](#contact)

<!-- ABOUT THE PROJECT -->

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

<div>
    <img alt="GitHub all releases" src="https://img.shields.io/github/downloads/owncast/owncast/total?style=for-the-badge">
	  <a href="https://hub.docker.com/r/owncast/owncast">
      <img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/owncast/owncast?style=for-the-badge">
	  </a>
    <a href="https://github.com/owncast/owncast/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22">
      <img alt="GitHub issues by-label" src="https://img.shields.io/github/issues-raw/owncast/owncast/good%20first%20issue?style=for-the-badge">
    </a>
    <a href="https://opencollective.com/owncast">
      <img alt="Open Collective backers and sponsors" src="https://img.shields.io/opencollective/all/owncast?style=for-the-badge">
    </a>
</div>

---

<!-- GETTING STARTED -->

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Go |
| Manifests detected | go.mod, go.sum |
| Files in snapshot | 1662 |
| Lines of code | 102355 |
| Dependency references | 382 |
| Dependencies by ecosystem | cargo: 6, go: 346, npm: 30 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| go | code.superseriousbusiness.org/activity | v1.19.0 | go.mod |
| go | github.com/andybalholm/cascadia | v1.3.4 | go.mod |
| go | github.com/aws/aws-sdk-go-v2 | v1.42.0 | go.mod |
| go | github.com/aws/aws-sdk-go-v2/credentials | v1.19.24 | go.mod |
| go | github.com/aws/aws-sdk-go-v2/service/s3 | v1.103.3 | go.mod |
| go | github.com/aws/smithy-go | v1.27.1 | go.mod |
| go | github.com/extism/go-sdk | v1.7.1 | go.mod |
| go | github.com/go-chi/chi/v5 | v5.2.4 | go.mod |
| go | github.com/go-fed/httpsig | v1.1.0 | go.mod |
| go | github.com/gobwas/glob | v0.2.3 | go.mod |
| go | github.com/gorilla/websocket | v1.5.3 | go.mod |
| go | github.com/grafov/m3u8 | v0.12.1 | go.mod |
| go | github.com/hashicorp/go-retryablehttp | v0.7.8 | go.mod |
| go | github.com/jellydator/ttlcache/v3 | v3.4.1 | go.mod |
| go | github.com/lestrrat-go/file-rotatelogs | v2.4.0+incompatible | go.mod |
| ... | (367 more) | | |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

<div>
    <img alt="GitHub all releases" src="https://img.shields.io/github/downloads/owncast/owncast/total?style=for-the-badge">
	  <a href="https://hub.docker.com/r/owncast/owncast">
      <img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/owncast/owncast?style=for-the-badge">
	  </a>
    <a href="https://github.com/owncast/owncast/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22">
      <img alt="GitHub issues by-label" src="https://img.shields.io/github/issues-raw/owncast/owncast/good%20first%20issue?style=for-the-badge">
    </a>
    <a href="https://opencollective.com/owncast">
      <img alt="Open Collective backers and sponsors" src="https://img.shields.io/opencollective/all/owncast?style=for-the-badge">
    </a>
</div>

---

<!-- GETTING STARTED -->

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

*Excerpt from upstream `CONTRIBUTING.md`:*

# Help contribute to Owncast!

Owncast is a growing open source project that is giving freedom, flexibility and fun to live streamers.
And while we have a small team of kind, talented and thoughtful volunteers, we have gaps in our skillset that we’d love to fill so we can get even better at building tools that make a difference for people.

We abide by our [Code of Conduct](https://owncast.online/contribute/) and feel strongly about open, appreciative, and empathetic people joining us.
We’ve been very lucky to have this so far, so maybe you can help us with your skills and passion, too!

There is a larger, more detailed, and more up-to-date [guide for helping contribute to Owncast on our website](https://owncast.online/help/).

## Before Submitting a PR

For web changes, from the `web/` directory:

```bash
npm run check              # Verify your code will pass CI
npm run lint && npm run format   # Auto-fix errors
```

For Go changes, from the project root:

```bash
make lint && make fmt
```

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2020-2023 Gabe Kangas

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `OWNCAST` (category: MOVIES MEDIA)
- **Upstream URL:** https://github.com/owncast/owncast
- **Pinned commit (SHA):** `cd64bdf44f11998e71e6c4e9ac522ea4a8f2dd1a`
- **Branch:** develop
- **Pin provenance:** GitHub API commits/develop. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`180cd81ebdef138cbcf62aba1c3a84dec08964e569cab100f5563f650a2dafad`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

