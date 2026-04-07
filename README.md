# Rocket Flight Computer

### DIY avionics that log altitude, acceleration, and rotation during a model rocket flight.

**Status:** 🔴 Planning — Architecture designed, awaiting parts

---

## What Is This?

A custom-built flight data recorder that rides inside a model rocket. An Arduino Nano reads sensors during flight — accelerometer, gyroscope, and barometric altimeter — and logs the data to a micro SD card. After recovery, we pull the SD card and graph the flight profile: altitude over time, acceleration forces during launch, rotation rates, and temperature.

This is real avionics built from scratch. The same fundamental approach is used in amateur rocketry competitions and even professional sounding rockets — just at a smaller scale.

---

## Sensors & Data

| Sensor | What It Measures | Data Output |
|--------|-----------------|-------------|
| MPU6050 | Acceleration (3-axis) + Gyroscope (3-axis) | Launch G-forces, spin rate, orientation |
| BMP280 | Barometric pressure + Temperature | Altitude (calculated from pressure), air temp |
| SD Card Module | — | Stores all data at high sample rate for post-flight analysis |

---

## Team Split

**Ivan Martinez (Flight Software):** Arduino code for sensor reading, SD card logging, data sampling rate optimization, post-flight Python scripts for graphing and analysis.

**Oskar Trujillo (Rocket & Hardware):** Estes rocket assembly, 3D printed nose cone payload bay adapter, flight computer physical wiring and mounting, launch operations, recovery.

---

## Build Phases

### Phase 1: Circuit Design ✅ Complete
- Sensor wiring schematic designed
- I2C bus layout for MPU6050 + BMP280
- SD card module SPI connection mapped

### Phase 2: Flight Computer Build 🔲 Awaiting Parts
- Wire MPU6050 + BMP280 + SD card to Arduino Nano
- Write data logging firmware
- Bench test: verify sensor readings and SD write speed

### Phase 3: Rocket Prep 🔲 Awaiting Parts
- Assemble Estes rocket kit
- 3D print nose cone payload adapter
- Fit flight computer into payload bay
- Verify center of gravity with payload

### Phase 4: Launch & Data 🔲 Upcoming
- Pre-flight checklist and safety review
- Launch with C6-5 motors
- Recover rocket and pull SD card
- Graph altitude, acceleration, and rotation curves

### Phase 5: Iterate 🔲 Future
- Active parachute deployment based on altimeter
- Live telemetry via radio module
- Higher altitude motors

---

## Parts List

| Part | Qty | Est. Cost | Who Buys |
|------|-----|-----------|----------|
| Estes Hi Flier Rocket Kit | 1 | $30 | Oskar |
| Estes C6-5 Motors (3-pack) | 1 | $12 | Oskar |
| BMP280 Barometric Sensor | 1 | $4 | Ivan |
| Micro SD Card Module + Card | 1 | $6 | Ivan |
| Arduino Nano | 1 | $8 | Ivan |
| 3.7V LiPo Battery (500mAh) | 1 | $5 | Ivan |
| Launch Pad + Controller | 1 | $15 | Oskar |
| **Total** | | **~$80** | |

*Note: MPU6050 already owned (included in SunFounder kit)*

---

## Links

- 🏠 [Forge Two Engineering](https://github.com/ForgeTwoEngineering)
- 📺 [YouTube — Build Journey](https://www.youtube.com/channel/UCjRHb705PTnDNKvWwySeZPQ)
- 📧 forgetwoengineering@gmail.com
