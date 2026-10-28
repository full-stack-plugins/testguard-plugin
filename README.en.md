# TestGuard (验收测试防护)

> This wrapper has not connected the separate engine: `check` returns `DESIGN_ONLY` with exit code 3, without invoking the engine or producing passing evidence. Engine functionality does not establish wrapper functionality.

**Version**: 0.1.1 · **License**: Apache-2.0 · **Skills**: 1

[简体中文](README.md)

## Positioning

TestGuard is an independent plugin in the Partme Guard family. Its command prefix is testguard. It is installed, versioned and executed independently.

## CLI Commands

| Command | Type |
| :--- | :--- |
| version | 独立入口 |
| doctor | 独立入口 |
| status | 独立入口 |
| discover | 独立入口 |
| check | 独立入口 |
| init | 独立入口 |

## Installation

Select plugin ID `testguard` from the [Full Stack Plugins marketplace](https://github.com/partme-ai/full-stack-plugins). The repository name `testguard-plugin` is not the plugin ID. The installation ref is `v0.1.1`; whether a host exposes `bin/` on PATH requires host-specific verification.

## Quick Start

~~~bash
testguard version
testguard doctor
testguard status
~~~

## Current Status

This wrapper has not connected the separate engine: `check` returns `DESIGN_ONLY` with exit code 3, without invoking the engine or producing passing evidence. Engine functionality does not establish wrapper functionality.

No PASS without real execution evidence. Unimplemented capabilities report DESIGN_ONLY or UNVERIFIED.

## Architecture

See product-docs/TestGuard/ and docs/ for command lifecycle, read-only checks and evidence boundaries.

## Boundaries

- Not merged into a single Partme Guard command.
- Does not replace another Guard's domain decision.
- Does not auto-commit, auto-push or modify user code.

## Verification

~~~bash
sh bin/testguard version
# Expected: DESIGN_ONLY and exit code 3
sh bin/testguard check
~~~

## License

Apache-2.0
