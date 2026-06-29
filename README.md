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

| Category | Device Used | Description |
| --- | --- | --- |
| Computer | LubanCat 4 (RK3588S2) | Main onboard computer for system control, computation, and device coordination |
| LiDAR | Livox MID360s | 3D sensing module for spatial perception and environment mapping |
| Camera | Hikvision MV-CS016-10GC x4 | Four industrial cameras for multi-view image capture |
| IMU | ICM40609 | Inertial measurement unit integrated inside the MID360s module |
| GNSS Receiver | u-blox F9P | High-precision positioning receiver for global navigation data |
| Antenna | Beitian BT-256 | GNSS antenna used with the positioning receiver |
| Network Switch | Qiandezhi commercial 1000 Mbps gigabit switch | Gigabit wired network hub for onboard device communication |
| Power | 4800 mAh lithium battery | Portable battery power source for the device system |

Detailed device notes, quantities, interfaces, and open items are maintained in
[`hardware/README.md`](hardware/README.md).

## 3D Models

The project includes a 3D preview of the device and the source CAD files used
for mechanical design and 3D printing. The full device assembly is provided as
[`Device.STEP`](models/device/Device.STEP), and the handheld mold parts are
available as [`bottom_new.STEP`](models/handheld/bottom_new.STEP) and
[`top_new.STEP`](models/handheld/top_new.STEP). These files are stored under
the [`models/`](models/) directory, with the animated preview shown below.

![3D model preview](docs/assets/device-3d-model.gif)

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
