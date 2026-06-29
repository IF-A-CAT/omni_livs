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

The project uses the following device categories. Replace the `TBD` entries
with the exact device names, model numbers, and links as the hardware list is
finalized.

| Category | Devices Used | Purpose | Status |
| --- | --- | --- | --- |
| Controller | TBD | Main control and computation | Planned |
| Sensors | TBD | Data collection and environment/device sensing | Planned |
| Actuators | TBD | Motion, switching, or physical output | Planned |
| Communication | TBD | Wired or wireless data transfer | Planned |
| Power | TBD | Power supply, conversion, and protection | Planned |
| Mechanical Parts | TBD | Frame, enclosure, mounting, and fixtures | Planned |
| Tools and Accessories | TBD | Assembly, testing, calibration, and maintenance | Planned |

Detailed device notes should be added in [`hardware/README.md`](hardware/README.md).

## 3D Models

The 3D models used by the project should be stored under the `models/`
directory. Each model should include the editable source format when possible
and an export format for fabrication or preview.

| Model Name | Related Device/Part | Recommended Format | Repository Path | Status |
| --- | --- | --- | --- | --- |
| Enclosure | Mechanical enclosure | STEP, STL, GLB | `models/enclosure/` | TBD |
| Mounting Bracket | Device mounting part | STEP, STL | `models/mounting-bracket/` | TBD |
| Device Assembly | Full device assembly preview | STEP, GLB | `models/assembly/` | TBD |

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
