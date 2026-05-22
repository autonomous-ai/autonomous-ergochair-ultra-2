# Electronics

All the electronics for the smart chair.

## Folders

- `schematics/` — circuit diagrams (PDF + KiCad source)
- `pcb/` — PCB design files and Gerber zips for fab
- `bom/` — parts list (CSV)
- `wiring/` — wiring diagrams, pinouts, connector maps

## Main Parts (typical)

- **MCU** — ESP32-S3 (Wi-Fi + BLE in one chip)
- **Posture sensor (seat)** — pressure mat: 4× FSR-402 or a 16-cell Velostat mat into an ADS1115
- **Posture sensor (back / recline angle)** — MPU-6050 or BMI270 IMU on the back-frame
- **Lumbar pump** — 6 V mini diaphragm air pump + 2-way solenoid valve, driven by N-channel MOSFET
- **Bladder pressure feedback** — BMP280 plumbed to the bladder line
- **Stand-up reminder** — small vibration motor in the seat pan (haptic) + RGB LED ring under the gas cylinder
- **Power** — 5 V 2 A USB-C input + 18650 li-ion (for "wireless" runtime); optional always-on USB power supply
- **Charging** — TP4056 + 5 V boost (MT3608) for the pump rail

Everything runs at 3.3 V logic / 5 V pump rail / 6 V analog pump motor.

## Pinout (typical, ESP32-S3 DevKit)

| Function | GPIO | Notes |
|---|---:|---|
| Pump MOSFET gate | 4 | PWM, low-side |
| Valve MOSFET gate | 5 | digital |
| Haptic motor | 6 | PWM |
| RGB LED ring (WS2812) | 7 | data |
| I²C SDA (IMU + BMP280 + ADS1115) | 8 | shared bus |
| I²C SCL | 9 | shared bus |
| Battery voltage sense | 1 (ADC1_CH0) | divider 100k/100k |
| User button | 0 | boot button reused |

See `electronics/wiring/` for the full pinout table.

## Safety

- 18650 cells must be matched and protected. Use a protection board.
- The pump and valve can backfeed inductive spikes. Use flyback diodes (1N4007 or similar).
- Charging IC must have thermal shutdown. Don't omit it.
- Always disconnect the battery before re-wiring.

See `bom/parts.csv` for the full list.
