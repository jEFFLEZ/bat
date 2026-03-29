# @funeste38/bat

`bat` is the published adaptive request-control package from the Funesterie ecosystem.

It gives you a small vocabulary of runtime components to observe latency, classify response quality, adapt request behaviour and rotate channels when a single path becomes unreliable.

## Install

```bash
npm install @funeste38/bat
```

## Core primitives

- `Bat`: raw sensing and RTT capture
- `Ears`: qualitative analysis of answers or channel noise
- `Wings`: adaptation logic, pacing and cooldown
- `Fangs`: multi-channel execution
- `Inversion`: escape hatch when BAT should be bypassed

## Quick example

```ts
import { Bat, Ears, Wings, Fangs } from "@funeste38/bat";

const bat = new Bat();
const ears = new Ears();
const wings = new Wings();
const fangs = new Fangs({ channels: [] });
```

## Use cases

- resilient proxy rotation
- multi-provider AI calling
- local tool execution with adaptive retry logic
- experimental orchestration around unstable channels

## Development

```bash
npm install
npm run build
npm test
```

## Local references

- `src/demo.ts`
- `test/basic.test.js`

## Good next improvements

- document concrete HTTP channel examples
- add typed events for telemetry and scoring
- expose a higher-level orchestrator preset for QFLUSH
