# Firmware Architecture

## Overview
The firmware is a single-loop event-driven keypad handler:

1. Initialize 12 LED pins as outputs and set LOW in `setup()`.
2. Poll keypad in `loop()` with `keypad.getKey()`.
3. If key detected, execute a `switch` statement that maps key to LED action.
4. Sleep briefly (`delay(10)`) for stable polling.

## Source Layout
- `src/main.cpp`: Original core logic (preserved behavior)
- `include/`: extension point for future headers
- `docs/wiring.md`: electrical mapping and pinout
- `README.md`: build/flash/simulation guidance

## Behavior Matrix
| Key | Action |
|---|---|
| `1..8` | Turn ON corresponding blue LED |
| `9` | Turn ON all blue LEDs (1..8) |
| `0` | Turn OFF all blue LEDs (1..8) |
| `A..D` | Turn ON corresponding red LED |
| `*` | Turn ON all red LEDs (A..D) |
| `#` | Turn OFF all red LEDs (A..D) |

## Design Notes
- No debouncing layer beyond keypad library internals and 10ms loop delay.
- State is implicit in GPIO output levels (no separate state machine).
- No Wi-Fi, interrupts, RTOS, DMA, or multicore usage.

## Portability Note
The code is Arduino-style (`setup()/loop()`, `digitalWrite`, `pinMode`, `Keypad.h`).
For pure Pico SDK projects, an adaptation layer or Arduino-Pico environment may be required during build integration, but logic remains unchanged.
