# Void Lake Fusion 4 (VLF4)

SRAD Avionics from the [McMaster Rocketry Team](https://www.macrocketry.ca/)

![](images/a.jpg)

![](images/b.jpg)

## Selling point

- Pyro short circuit protection
- Molex nano-fit connectors
- 1W LoRa, 100km+ LoS range
- GPS + IMU + baro sensor fusion, reducing the chance of ejecting prematurely
- Modern 3D visualizer
- Small
- Open source firmware
- Relatively cheap

## Pyro
- 3 pyro channels, each 8A continuous (current limited by the connector due to size)
- pyro channels not connected to battery+ when not firing (unlike raven)
- continuity detection
- short circuit protection

## Sensors
- MCU: STM32H723
- IMU 1: ±2000deg/s ±16g (LSM6DSMTR)
- IMU 2: ±100g (H3LIS100DLTR)
- Magnetometer: MMC5603NJ
- Barometer: max altitude 30km (MS5607)
- Storage: 64MB NOR Flash (W25Q512JVFIQ)
- GPS: L80RE-M37
- Radio: 1W LoRa (e22-900m30s)

## Connectivity
- 2 buzzers for stereo sound
- usb type-c
- battery: 2 pin molex nano-fit
- power & arming switch: 4 pin molex nano-fit (no large current is carried over switches)
- pyro: 6 pin molex nano-fit
- extension: 8 pin molex nano-fit:
  - ground: 1 pin
  - power out (battery voltage) (only provides power out if the power switch is turned on): 1 pin
  - serial: 2 pins
  - CAN: 2 pins
  - GPIO: 2 pins
- Serial Wire Debug: 5 pin molex pico-clasp
- SMA antenna connector

## Software (WIP, to be open sourced)
- Async embedded rust
