# Pico W Keypad-to-LED Controller

Documentation-first repository layout for a **Raspberry Pi Pico W (RP2040)** project that reads a **4x4 matrix keypad** and controls **12 LEDs**.

> Core behavior is preserved from the provided source: each key event turns on/off one LED or a group of LEDs.

## Project Overview
This project maps keypad keys (`0-9`, `A-D`, `*`, `#`) to LED control actions on the Pico W GPIOs.

- Keys `1..8` turn on one blue LED each
- Key `9` turns on all blue LEDs (`1..8`)
- Key `0` turns off all blue LEDs (`1..8`)
- Keys `A..D` turn on one red LED each
- Key `*` turns on all red LEDs (`A..D`)
- Key `#` turns off all red LEDs (`A..D`)

No Wi-Fi logic is used by the current firmware.

## Recommended Repository Structure (Pico SDK / C++)

```text
.
├── CMakeLists.txt
├── README.md
├── include/
│   └── README.md
├── src/
│   └── main.cpp
└── docs/
    ├── architecture.md
    └── wiring.md
```

## Features
- 4x4 keypad scan via GPIO matrix pins
- Deterministic key-to-LED mapping
- 12 independent LED outputs
- Group on/off controls (blue bank, red bank)
- Wokwi-compatible wiring and pinout

## Components List (from `diagram.json`)
- 1x Raspberry Pi Pico / Pico W form factor board (`wokwi-pi-pico`)
- 1x 4x4 membrane keypad (`wokwi-membrane-keypad`)
- 12x LEDs
  - 8 blue LEDs (labels `1..8`)
  - 4 red LEDs (labels `A..D`)
- 12x 220Ω resistors (LED current limiting)
- 4x 1kΩ resistors (keypad row pull-up network to 3V3)
- Shared GND and 3V3 rails

## GPIO Mapping Summary
See full mapping in [docs/wiring.md](docs/wiring.md).

## Build and Flash (Real Pico W with Pico SDK)

### 1) Prerequisites
- `cmake`
- `gcc-arm-none-eabi`
- Pico SDK cloned locally

Example:
```bash
git clone https://github.com/raspberrypi/pico-sdk
export PICO_SDK_PATH=/absolute/path/to/pico-sdk
```

### 2) Build
```bash
mkdir -p build
cd build
cmake ..
cmake --build .
```

### 3) Flash
1. Hold **BOOTSEL** while plugging Pico W over USB.
2. Copy generated `keypad_led_controller.uf2` to the mounted `RPI-RP2` drive.
3. Board reboots and runs firmware.

## Run in Wokwi
1. Create a new **Raspberry Pi Pico** project in Wokwi.
2. Paste the provided `diagram.json` into `diagram.json`.
3. Place firmware logic equivalent to `src/main.cpp` in the simulator-supported sketch.
4. Start simulation and press keypad buttons.

> Note: Wokwi uses a Pico model in the diagram; the GPIO behavior is compatible with Pico W for this use case.

## Wi-Fi Note
Pico W Wi-Fi hardware is present but **unused** in this application. If Wi-Fi is added later, keep credentials out of source control (e.g., separate ignored config file).

## Source of Core Logic
The behavior documented here comes directly from the provided keypad/LED switch-case program and was not functionally changed.
