# Firmware

Code that runs on the chair's microcontroller.

## Target

- ESP32-S3 (default)
- Build with PlatformIO or Arduino IDE

## Folders (add as you go)

- `src/` — main code
- `lib/` — libraries
- `include/` — headers
- `platformio.ini` — PlatformIO config

## What it does

- Reads the seat-pan pressure mat (16 cells via ADS1115) at 10 Hz
- Reads the back IMU for recline angle and vibration (slouch detection)
- Reads bladder pressure (BMP280) for lumbar feedback
- Drives the air pump + valve via MOSFETs to hold a target lumbar pressure
- Posts BLE notifications: posture score, sit time, lumbar pressure
- Exposes a small Wi-Fi web UI for setup + OTA

## Build

```
pio run
pio run -t upload
```

## Flash by USB

1. Plug in the chair controller via USB-C (under the seat pan)
2. `pio run -t upload`
3. Open serial monitor: `pio device monitor -b 115200`

## OTA Update

Once connected to Wi-Fi, you can update over the air. See `docs/ota.md`.

## BLE GATT (planned)

| Service UUID | Characteristic | Direction | Notes |
|---|---|---|---|
| `0xA000` | posture_score | notify | 0-100, 1 Hz |
| `0xA000` | sit_time_minutes | notify | resets on stand-up |
| `0xA001` | lumbar_target_kpa | write | sets desired bladder pressure |
| `0xA001` | lumbar_actual_kpa | notify | measured |

Numbers are placeholder until the app is in repo.
