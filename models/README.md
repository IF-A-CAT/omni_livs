# 3D Models

This directory stores 3D model files used by the project.

## Suggested Layout

```text
models/
  device/
    Device.STEP
  handheld/
    bottom_new.STEP
    top_new.STEP
```

## File Guidelines

- Keep editable CAD source files when possible, such as `STEP`, `FCStd`, or
  native CAD project files.
- Include fabrication/export files when useful, such as `STL`, `OBJ`, or `GLB`.
- Use clear file names that include the part name, version, and date when
  appropriate.
- Use Git LFS for large model files.

## Model Inventory

| Model Name | Device/Part | Source File | Export File | Status |
| --- | --- | --- | --- | --- |
| Device 3D Model | Full device assembly | [`device/Device.STEP`](device/Device.STEP) | [`../docs/assets/device-3d-model.gif`](../docs/assets/device-3d-model.gif) | Available |
| Handheld Bottom Mold | 3D-printing mold part | [`handheld/bottom_new.STEP`](handheld/bottom_new.STEP) | TBD | Available |
| Handheld Top Mold | 3D-printing mold part | [`handheld/top_new.STEP`](handheld/top_new.STEP) | TBD | Available |
