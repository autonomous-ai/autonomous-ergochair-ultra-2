# Assembly Guide

How to build the chair, step by step.

## Before You Start

1. Read the full guide first
2. Get all parts (`bom/parts.csv` and `electronics/bom/parts.csv`)
3. Print all CAD parts (`cad/stl/`)
4. Tools needed: hex keys (4 / 5 / 6 mm), Phillips driver, rubber mallet, soldering iron, multimeter, heat-shrink + gun

## Time

About 3-5 hours for a first build (chair frame ~1 h, electronics + integration ~3 h, calibration ~1 h).

## Steps

### Step 1 — Caster spider + casters

Press-fit the 5 casters into the spider. Use the rubber mallet — no glue. Photo: `photos/step-01.jpg`

### Step 2 — Gas cylinder

Drop the class-4 gas cylinder into the spider's center socket. Friction-fit only; the chair's weight locks it in. Photo: `photos/step-02.jpg`

### Step 3 — Tilt mechanism + seat pan

Bolt the tilt mechanism to the underside of the seat pan (4× M8). Set tilt tension to neutral for now. Photo: `photos/step-03.jpg`

### Step 4 — Seat pressure mat

Lay the Velostat / FSR mat into the seat-pan pocket (`cad/drawings/seat-pan_drawing.pdf`). Route the 17-wire ribbon (16 sense + 1 ground) through the side channel toward the controller bay. Photo: `photos/step-04.jpg`

### Step 5 — Back frame + lumbar bladder

Bolt the back frame to the tilt mechanism. Mount the lumbar bladder behind the mesh using the `lumbar-bladder-mount` printed bracket. Plumb the air line (4 mm OD silicone) down the back frame toward the controller bay. Photo: `photos/step-05.jpg`

### Step 6 — IMU on the back frame

Mount the BMI270 / MPU-6050 breakout to the back frame, X-axis pointing up. Run its I²C cable down to the controller bay. Photo: `photos/step-06.jpg`

### Step 7 — Armrests + headrest

Slide armrest yokes onto the seat frame and secure with the side hex bolts. Slide the headrest posts down into the back-frame sockets. Photo: `photos/step-07.jpg`

### Step 8 — Controller housing + electronics

Bolt the printed `controller-housing` to the underside of the seat pan. Land all three cable bundles (pressure mat, back IMU + bladder pressure, pump/valve) into the main board's connectors. Battery in last.

### Step 9 — LED ring under the spider

Snap the WS2812 ring around the gas-cylinder hub on the spider. Route data + power up through the gas-cylinder cap into the controller bay. Photo: `photos/step-09.jpg`

### Step 10 — Flash firmware

See `firmware/README.md`. First flash by USB-C; subsequent updates can be OTA.

### Step 11 — First boot and calibration

1. Sit on the chair with the firmware in calibration mode (hold the boot button while booting)
2. Sit normally for 30 s — this captures the "good posture" baseline pressure pattern
3. Slouch forward for 10 s — this captures the "bad posture" pattern
4. Pump the lumbar to your preferred firmness — the firmware learns the target kPa
5. Stand up; chair should detect zero pressure and stop the sit timer

### Step 12 — Done

Test:
- BLE pairs with the phone app
- Lumbar inflates and holds pressure
- Slouching for >10 s triggers a haptic buzz
- Stand-up reminder fires after the configured sit interval

## Troubleshooting

- Pump runs forever → BMP280 not reading, check I²C address conflict (0x76 vs 0x77)
- IMU reports flatline → wiring; check 3.3 V to the breakout
- LED ring is dim or flickering → data line should be 5 V; level-shift if your ring needs it
- Chair won't recognize "stood up" → pressure mat dead cell or stuck connector

More in `docs/troubleshooting.md`.
