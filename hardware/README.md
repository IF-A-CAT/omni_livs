# Hardware

This directory documents the device categories, device inventory, and hardware
assets used by the project.

The hardware documentation is organized so contributors can quickly understand
which components are already selected, what each component does, and which
technical details still need to be completed.

## Hardware Overview

| Area | Current Status | Related Files or Notes |
| --- | --- | --- |
| Full device assembly | Available | [`../models/device/Device.STEP`](../models/device/Device.STEP) |
| 3D model preview | Available | [`../docs/assets/device-3d-model.gif`](../docs/assets/device-3d-model.gif) |
| Handheld bottom mold | Available | [`../models/handheld/bottom_new.STEP`](../models/handheld/bottom_new.STEP) |
| Handheld top mold | Available | [`../models/handheld/top_new.STEP`](../models/handheld/top_new.STEP) |
| Core electronics | Selected | See the device inventory below |
| Power and wiring | Partially specified | Battery capacity is listed; voltage, connectors, and protection details should be added |

## Device Inventory

| ID | Category | Device / Part | Model or Part Number | Quantity | Function | Status |
| --- | --- | --- | --- | --- | --- | --- |
| CTRL-001 | Controller | LubanCat 4 | RK3588S2 | 1 | Main control, computation, and system coordination | Selected |
| LIDAR-001 | LiDAR | Livox MID360s | MID360s | 1 | 3D spatial perception and environment sensing | Selected |
| CAM-001 | Camera | Hikvision industrial camera | MV-CS016-10GC | 4 | Multi-view image capture | Selected |
| IMU-001 | IMU | Inertial measurement unit inside MID360s | ICM40609 | 1 | Inertial measurement for motion and orientation reference | Selected |
| GNSS-001 | GNSS Receiver | u-blox F9P receiver | F9P | 1 | High-precision positioning | Selected |
| ANT-001 | Antenna | Beitian GNSS antenna | BT-256 | 1 | GNSS signal reception | Selected |
| NET-001 | Network Switch | Qiandezhi commercial gigabit switch | 1000 Mbps | 1 | Wired data transfer between onboard devices | Selected |
| PWR-001 | Power | Lithium battery | 4800 mAh | 1 | Portable power supply | Selected |
| MECH-001 | Mechanical Structure | Full device assembly | [`Device.STEP`](../models/device/Device.STEP) | 1 | Main CAD model for the complete device | Available |
| MECH-002 | 3D-Printing Mold | Handheld bottom mold | [`bottom_new.STEP`](../models/handheld/bottom_new.STEP) | 1 | STEP file for 3D printing or mold fabrication | Available |
| MECH-003 | 3D-Printing Mold | Handheld top mold | [`top_new.STEP`](../models/handheld/top_new.STEP) | 1 | STEP file for 3D printing or mold fabrication | Available |

## Device Categories

| Category | Role in the System | Included Components |
| --- | --- | --- |
| Control and Computation | Runs the main software stack and coordinates connected devices | LubanCat 4 |
| Perception | Captures spatial and visual data from the environment | Livox MID360s, Hikvision cameras |
| Positioning and Motion | Provides positioning, attitude, and motion reference data | u-blox F9P, Beitian BT-256, ICM40609 |
| Communication | Connects high-bandwidth onboard devices | Qiandezhi 1000 Mbps gigabit switch |
| Power | Supplies portable operating power | 4800 mAh lithium battery |
| Mechanical Assets | Provides the physical assembly and fabrication files | Device STEP model, handheld mold STEP files |

## Open Hardware Details

The following details should be added when they are finalized:

| Item | Details Needed |
| --- | --- |
| Controller | Operating system image, power input, network interface, and peripheral connections |
| LiDAR | Mounting orientation, data interface, power input, and calibration notes |
| Cameras | Lens model, trigger mode, exposure settings, connection method, and mounting positions |
| GNSS | Receiver board variant, antenna cable, coordinate frame, and correction-data method |
| Network switch | Port count, power input, mounting method, and device connection map |
| Battery | Nominal voltage, discharge rating, connector type, charger, and protection method |
| Wiring | Cable types, connector names, power distribution, and grounding strategy |

## Model Assets

The current mechanical assets are stored under [`../models/`](../models/):

- Full device assembly: [`../models/device/Device.STEP`](../models/device/Device.STEP)
- Handheld bottom mold: [`../models/handheld/bottom_new.STEP`](../models/handheld/bottom_new.STEP)
- Handheld top mold: [`../models/handheld/top_new.STEP`](../models/handheld/top_new.STEP)

Large CAD files can be moved to Git LFS later if the repository grows beyond
normal GitHub file-size limits.
