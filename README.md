<p align="center">
  <img src="https://imagerry.com/icons/icon-512x512.png" alt="Imagerry CLI" width="80" height="80" />
</p>

<h1 align="center">Imagerry CLI</h1>

<p align="center">
  Fast, privacy-first image customizer, formatter, and styling engine for your terminal.
</p>

<p align="center">
  <a href="https://imagerry.com/cli"><img src="https://img.shields.io/badge/docs-imagerry.com%2Fcli-1f6feb" alt="Documentation" /></a>
  <a href="https://www.npmjs.com/package/@imagerry/cli"><img src="https://img.shields.io/npm/v/@imagerry/cli?color=cb0000&label=npm" alt="npm package" /></a>
  <img src="https://img.shields.io/badge/runs%20locally-100%25%20private-000000" alt="100% Local & Private" />
  <img src="https://img.shields.io/badge/license-proprietary-success" alt="License" />
</p>

---

## What is it?

**Imagerry CLI** is the command-line interface for [Imagerry](https://imagerry.com). It allows developers, designers, and automated pipelines to format, compress, style, watermark, and generate mockups directly from the terminal.

Images are processed **100% locally** using compiled native Skia graphics engine bindings—your files are never uploaded to any cloud server.

- **Modern Built-in Presets** — `mesh`, `gradient`, `cyberpunk`, `sunset`, `studio`, `aurora`, and `default`
- **Multi-Format Encoding** — Lossless PNG, high-efficiency WebP, and quality-tuned JPEG
- **Direct CLI Overrides** — Adjust `--padding`, `--radius`, `--shadow`, `--bg-color`, `--ratio`, and text overlays on the fly
- **Parallel Batch Processing** — Convert entire directories or glob patterns with multi-core concurrency
- **Unix Streaming Pipelines** — Seamless `stdin` and `stdout` binary piping (`cat in.png | imagerry -o - > out.webp`)
- **Project Defaults** — Interactive `imagerry init` wizard to scaffold team configs (`imagerry.config.json`)
- **Shell Autocompletion** — Native tab completions for GNU Bash, Zsh, and Fish
- **Local HTTP Microservice** — Spin up a local REST API server with `imagerry serve`
- **AI Agent MCP Server** — Native Model Context Protocol tools for Cursor, Claude Desktop, and Zed

---

## Installation

### Standalone Binary (Zero Node.js Required)

```bash
# macOS & Linux
curl -fsSL https://imagerry.com/cli/install.sh | bash

# Windows (PowerShell)
irm https://imagerry.com/cli/install.ps1 | iex
```

### npm Global Install

```bash
npm install -g @imagerry/cli
```

---

## Quick Examples

```bash
# 1. Style an image with the vibrant mesh gradient preset
imagerry -i screenshot.png -o output.webp --preset mesh

# 2. Convert and compress with custom quality & aspect ratio
imagerry -i photo.png -o photo.jpg -q 85 --ratio 16:9 --padding 40

# 3. Stream binary image data through Unix pipe
cat input.png | imagerry -i - -o - --format webp --preset gradient > output.webp

# 4. Batch process an entire directory of screenshots in parallel
imagerry -i ./screenshots -o ./dist --preset cyberpunk --format webp

# 5. Interactive project configuration wizard
imagerry init

# 6. Enable shell tab autocompletion (Zsh / Bash / Fish)
eval "$(imagerry completion zsh)"
```

---

## Documentation

Full documentation, flag references, HTTP API schemas, and MCP assistant configuration guides are available at:

[https://imagerry.com/cli](https://imagerry.com/cli)

---

## Licensing

Imagerry CLI includes a **Free Tier** (15 free conversions / day). For unlimited batch automation, CI/CD pipelines, and hosting the self-hosted API/MCP server, an **[Imagerry Pro](https://imagerry.com/pro)** license is required.

---

## Links

- **Website**: [https://imagerry.com](https://imagerry.com)
- **CLI Docs**: [https://imagerry.com/cli](https://imagerry.com/cli)
- **JSON Schema**: [https://imagerry.com/schema/config.json](https://imagerry.com/schema/config.json)
- **Report Issues**: [https://github.com/imagerry-app/cli/issues](https://github.com/imagerry-app/cli/issues)
