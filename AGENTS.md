# MSM8953 SoC agent guide

This repository owns the shared MSM8953 / Snapdragon 632 resources: CPU topology,
DT platform configuration, and the DTSI included by MSM8953 board device trees.

## Read first

Read this README and the UniXNU [SoC support
guide](https://unixnu.com/porting/soc-support) before changing the port.

| Task | Required reading |
| --- | --- |
| SoC support | [Select and add SoC support](https://unixnu.com/porting/soc-support) |
| Hardware | [Device tree](https://unixnu.com/porting/device-tree), selected SoC README |
| Kernel | [Source and patches](https://unixnu.com/xnu/source-and-patches) |

## Work

Reusable controller code and shared platform operations belong here. Board-specific
wiring, memory and peripherals belong in the device repository (UniXNU-onclite).
Match the catalog component IDs and preserve runtime identifiers.

The firmware reference is ishakumari5/edk2-msm (onclite support), which is
edk2-porting based and built with `build.sh --device onclite`; it is not yet
integrated into the UniXNU Mu-Silicium firmware step.
