# Wiring (Raspberry Pi Pico W)

This wiring is derived from the provided Wokwi `diagram.json`.

## Assumptions
- Board in diagram is `wokwi-pi-pico`; mapping is valid for Pico W GPIO behavior.
- LED cathodes are tied to GND; GPIO drives anodes HIGH through 220Ω resistors.
- Keypad rows have 1k pull-up network to 3V3 (as drawn), and scanning is handled by the `Keypad` library.

## GPIO Pin Mapping

### Keypad
| Keypad Pin | Pico W GPIO |
|---|---|
| C1 | GP19 |
| C2 | GP18 |
| C3 | GP17 |
| C4 | GP16 |
| R1 | GP26 |
| R2 | GP22 |
| R3 | GP21 |
| R4 | GP20 |

### LED outputs (`ledPins[]` order)
| Logical LED | Label | Pico W GPIO |
|---|---|---|
| ledPins[0] | 1 | GP11 |
| ledPins[1] | 2 | GP10 |
| ledPins[2] | 3 | GP9 |
| ledPins[3] | 4 | GP8 |
| ledPins[4] | 5 | GP7 |
| ledPins[5] | 6 | GP6 |
| ledPins[6] | 7 | GP5 |
| ledPins[7] | 8 | GP4 |
| ledPins[8] | A | GP3 |
| ledPins[9] | B | GP2 |
| ledPins[10] | C | GP28 |
| ledPins[11] | D | GP27 |

## Power and Ground
- LED cathodes: common GND (`pico:GND.4` in diagram)
- Keypad pull-up chain (`rp1..rp4`, 1k each): tied to `pico:3V3`

## Serial Monitor (Wokwi)
- GP0 -> Serial RX
- GP1 -> Serial TX

Serial is wired in diagram but not used by the provided logic.
