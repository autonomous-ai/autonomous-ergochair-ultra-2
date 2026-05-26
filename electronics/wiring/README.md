# Wiring

How to connect everything.

Upload:
- Wiring diagrams (image or PDF)
- Pinout tables (markdown or CSV)
- Cable lists

Keep wire colors consistent across docs:
- Red = +V (battery / 5 V)
- Black = GND
- Yellow = signal / data (I²C SDA, single-ended sensor lines)
- Blue = signal / clock (I²C SCL)
- White = pump / valve control (digital from MCU)
- Green = haptic / LED data line

## Chair-specific cable runs

The controller housing sits under the seat pan. Three cable bundles leave it:

1. **Up the back-frame** → IMU + bladder BMP280 + bladder pump/valve
2. **Into the seat pan** → pressure mat (ADS1115 + 16 sense lines) + haptic motor
3. **Down the gas cylinder** → LED ring + USB-C charge port at the caster spider

Use 22 AWG silicone wire for everything that flexes (anywhere the back recline moves the cable). Solid-core breaks at the bend point within weeks.

> **Status: to be updated** — no wiring diagrams or pinout tables uploaded yet.
