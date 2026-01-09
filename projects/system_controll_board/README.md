# System Control Board Project

## Overview
The **System Control Board** is a general-purpose control platform designed to standardize and accelerate test fixture (rig) development. It integrates motor control, power conversion, relay switching, and common expansion interfaces (load cells, SD logging, display), enabling most rigs to be built around a single hardware base.

## Key Capabilities

### Motor Control Outputs
- **Up to 6× 12 V motors**
- **1× 24 V motor**
- **Up to 1× 60 V motor** (located in the **right-most corner** of the board)

### Power Architecture
Onboard regulation supports multi-rail operation for motors and logic:
- **Buck converter: 24 V → 12 V**
- **Buck converter: 12 V → 5 V**
- **Low-noise LDO: 5 V → 3.3 V**
  - Used to reduce noise on the **MCU (microcontroller) power rail**.

### Relay Switching
- **4× relays** onboard
- Relays are controlled using **5 V logic**
- **Level shifters** allow the MCU (3.3 V domain) to safely trigger the relay control circuitry

### Core MCU
- **STM32H753** selected for its wide range of peripherals and performance (timers, SPI, I2C, GPIO, etc.)

### Expansion / Add-On Support
- Optional support for **load cell amplifier(s)**
- **SD card module via SPI** (data logging)
- **Display support via SPI or I2C**

## Suggested Repository Structure
- `hardware/`
  - Schematics
  - PCB layout
  - Connector definitions
  - Assembly drawings
- `firmware/`
  - MCU firmware source
  - Board support package (BSP)
  - Peripheral drivers (motors, relays, SD, display)
- `docs/`
  - Bring-up procedure
  - Test plan + results
  - Revision notes
- `bom/`
  - Bill of Materials (BOM)
  - Alternate parts list (if applicable)

## Status
**In progress**

## Notes
This board is intended to be reusable across multiple test fixtures to minimize redesign effort and reduce wiring/bring-up time.
