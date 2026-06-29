# 2026project

An open-source repository for the 2026 device project.

This repository is intended to keep the project code, device information,
documentation, and 3D model assets in one public, reusable place.

## Repository Structure

```text
2026project/
  README.md          Project overview and public entry point
  LICENSE            Open-source license
  docs/              Design notes and user documentation
  hardware/          Device types, device list, and bill of materials
  models/            3D model files for devices and mechanical parts
  src/               Source code
  examples/          Example code and usage demos
```

## Device Types

The project currently uses the following core hardware components.

| Category | Device Used | Purpose | Status |
| --- | --- | --- | --- |
| Controller | LubanCat 4 (RK3588S2) | Main control, computation, and system coordination | Selected |
| LiDAR | Livox MID360s | 3D spatial perception and environment sensing | Selected |
| Camera | Hikvision MV-CS016-10GC x4 | Multi-view image capture | Selected |
| IMU | ICM40609 | Inertial measurement, integrated inside the MID360s module | Selected |
| GNSS Receiver | u-blox F9P | High-precision positioning | Selected |
| Antenna | Beitian BT-256 | GNSS signal reception | Selected |
| Network Switch | Qiandezhi commercial 1000 Mbps gigabit switch | Wired data transfer between onboard devices | Selected |
| Power | 4800 mAh lithium battery | Portable power supply | Selected |

Detailed device notes, quantities, interfaces, and open items are maintained in
[`hardware/README.md`](hardware/README.md).

## 3D Models

The project includes a 3D device model preview and the source CAD model file.

![3D model preview](docs/assets/device-3d-model.gif)

| Model Name | Related Device/Part | Recommended Format | Repository Path | Status |
| --- | --- | --- | --- | --- |
| Device 3D Model | Full device assembly | STEP, GIF | [`models/device/Device.STEP`](models/device/Device.STEP) | Available |
| Handheld Bottom Mold | 3D-printing mold part | STEP | [`models/handheld/bottom_new.STEP`](models/handheld/bottom_new.STEP) | Available |
| Handheld Top Mold | 3D-printing mold part | STEP | [`models/handheld/top_new.STEP`](models/handheld/top_new.STEP) | Available |

Recommended model formats:

- `STEP` or `FCStd` for editable CAD source files
- `STL` for 3D printing
- `OBJ` or `GLB` for web preview and visualization

Large 3D files should be managed with Git LFS when they become too large for
normal Git history.

## Getting Started

Clone the repository:

```bash
git clone https://github.com/IF-A-CAT/2026project.git
cd 2026project
```

Project-specific setup instructions will be added after the code structure is
finalized.

## Contributing

Contributions are welcome. Please keep changes organized by area:

- Code changes go in `src/`
- Example usage goes in `examples/`
- Device information goes in `hardware/`
- 3D models go in `models/`
- Design and usage documentation goes in `docs/`

## License

This project is released under the license included in [`LICENSE`](LICENSE).
