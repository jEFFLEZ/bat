# @funeste38/bat

`bat` is the adaptive request-control family for Funesterie.

It models network or tool execution like a small reactive organism: it listens, classifies, adapts, retries carefully and learns which channels are worth trusting.

[![npm version](https://img.shields.io/npm/v/@funeste38/bat.svg)](https://www.npmjs.com/package/@funeste38/bat)
[![CI](https://github.com/jEFFLEZ/bat/actions/workflows/publish.yml/badge.svg)](https://github.com/jEFFLEZ/bat/actions)

## Repository layout

- `packages/bat` is the canonical npm package and the public source of truth
- `packages/bat-system` is a legacy/internal primitive set kept for compatibility and archaeology
- the repo root is currently a lightweight wrapper around the published package

## Canonical source of truth

If a runtime or adapter has to choose between the two trees, prefer `packages/bat`.

`packages/bat-system` still exists because it contains the older naming family (`BatEars`, `BatFangs`, etc.), but new integrations should not mix imports across both trees in the same file.

## Core concepts

- `Bat`: sonar and signal measurement
- `Ears`: response analysis and noise filtering
- `Wings`: adaptive behaviour such as retries, pacing and cooldown
- `Fangs`: multi-channel execution and channel rotation
- `Inversion`: fallback behaviour when the main strategy should be bypassed
- `Heart`, `Memory`, `Hormones`, `Immune`, `Sleep`: state and resilience helpers

## Quick example

```ts
import { Bat, Ears, Wings, Fangs } from "@funeste38/bat";

const bat = new Bat();
const ears = new Ears();
const wings = new Wings();
const fangs = new Fangs({ channels: [] });
```

## What this package is good at

- adaptive request orchestration
- experimentation with parallel or rotating channels
- local assistant runtimes that need resilience without heavyweight infrastructure

## Good next improvements

- formal metrics output for every adaptive decision
- richer presets for HTTP, tunnel and LLM workloads
- clearer channel health scoring
- integration examples with QFLUSH and Spyder

## Package docs

See [packages/bat/README.md](./packages/bat/README.md) for package-level usage.
