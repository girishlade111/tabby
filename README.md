<div align="center">

# 🐾 Tabby

[📚 Docs](https://tabby.tabbyml.com/docs/welcome/) • [💬 Slack](https://links.tabbyml.com/join-slack) • [🗺️ Roadmap](https://tabby.tabbyml.com/docs/roadmap/)

[English](/README.md) | [简体中文](/README-zh.md) | [日本語](/README-ja.md)

</div>

> Tabby is a self-hosted AI coding assistant, offering an open-source and on-premises alternative to GitHub Copilot.

This repository is a **fork of [TabbyML/tabby](https://github.com/TabbyML/tabby)**, maintained by Girish Lade — kept in sync with upstream for local experimentation and study.

## Features (upstream)

- **Self-contained** — no DBMS or cloud service required.
- **OpenAPI interface** — easy to integrate with existing infrastructure (e.g. Cloud IDE).
- **Consumer-grade GPUs** — runs on hardware you already own.
- **IDE clients** — VS Code, JetBrains and more (see `clients/`).

## Tech Stack

- **Backend:** Rust (`crates/`, workspace in `Cargo.toml`)
- **Frontend clients:** TypeScript (`clients/`, pnpm workspace)
- **CI:** GitHub Actions + codecov (`ci/`, `codecov.yml`)
- **Packaging:** Docker (`docker/`), Makefile targets

## Quick Start

### Server (from source)

```bash
cargo run --bin tabby
```

### Docker

```bash
docker run -it -p 8080:8080 -v $HOME/.tabby:/data tabbyml/tabby serve --model StarCoder-1B --device cpu
```

See the [official docs](https://tabby.tabbyml.com/docs/welcome/) for full installation and model options.

## Project Structure

```
crates/          # Rust backend (server, models, API)
clients/         # IDE extensions (VS Code, JetBrains, ...)
ee/              # enterprise-edition code (upstream)
experimental/    # experimental features
docker/          # container images
ci/              # CI scripts
```

## License

Apache 2.0 (upstream). See [LICENSE](./LICENSE).

---

Fork maintained by Girish Lade — https://ladestack.in
