# Codex ARM32 — experimental

Experimental GitHub Actions cross-build of the **original** [OpenAI Codex](https://github.com/openai/codex) Rust CLI for Linux ARMv7 (`arm-unknown-linux-gnueabihf`). Intended for Ubuntu armhf under Termux PRoot on a Galaxy J6+.

**Not officially supported.** Builds may fail due to upstream dependencies, platform assumptions or unavailable ARM32 native libraries. No compatibility or runtime success is guaranteed. The workflow does not patch upstream code and does not touch the FCC installation.

## Build

Open **Actions → Experimental Codex ARM32 → Run workflow**. Inspect logs. On success, download the `codex-linux-arm32-experimental` artifact. On failure, inspect the first compiler error. Artifacts must be tested on the target device before use.

## Security and resources

No API keys are needed for building. The workflow uses read-only repository permissions, pins the upstream revision through an input (defaults to `main`), limits build time, and uploads only a successfully built executable. Build output is not a verified release. GitHub Actions usage is subject to your account's quota and repository visibility.
