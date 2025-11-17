# @funeste38/bat 🦇
Adaptive request controller inspired by bats.

Components:
- Bat (sonar): measure RTT, classify signals.
- Ears: analyze response quality, origin, noise filtering.
- Wings: adapt behavior (speed, retries, abort, cooldown).
- Fangs: multi-channel parallel requests (proxy/IP rotation).
- Inversion: upside-down fallback, bypass BAT on failure.
- Heart: periodic ticks & safety cycle.
- Memory: short-term memory.
- Hormones: global stress level.
- Immune: ban unstable channels.
- Sleep: long recovery mode.

Usage example:

```javascript
import { Bat, Ears, Wings, Fangs } from '@funeste38/bat';
