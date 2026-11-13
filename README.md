# UniXNU MSM8953 support

Shared Qualcomm MSM8953 / Snapdragon 632 support for UniXNU: CPU topology and
DT platform resources shared by boards on this SoC (Redmi 7/onclite, Redmi 5
Plus/vince, and other MSM8953 devices).

`soc.toml` selects `ArmCpu` and `ArmDTPlatform`. Device repositories supply
memory layout, peripherals, firmware, power policy, and packaging.

## Contents

| Path | Contents |
| --- | --- |
| `soc.toml` | SoC profile and component selection |
| `configs/msm8953.config` | Kernel configuration fragments |
| `dts/msm8953.dtsi` | Shared hardware resources |
| `patches/xnu/series` | Ordered SoC patches (empty) |
| `kits/` | Shared platform operations (none yet) |

Build through the UniXNU CLI. See the [device repository
specification](https://unixnu.com/porting/device-repository),
[device-tree specification](https://unixnu.com/porting/device-tree), and
[component catalog](https://unixnu.com/reference/components).

## Firmware reference

UEFI bring-up for MSM8953/onclite is tracked separately in
[ishakumari5/edk2-msm](../edk2-msm), which already carries onclite device
support (`Platform/Xiaomi/msm8953/onclite.dsc`, `onclite.fdf.inc`,
`Silicon/Qualcomm/msm8953/`, `FdtBlob_compat/onclite.dtb`). That repository is
edk2-porting/Renegade based and is built with its own `build.sh --device
onclite`; integrating it into the UniXNU Mu-Silicium firmware step is part of
the onclite port.
