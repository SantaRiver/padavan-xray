# padavan-xray

Prebuilt [Xray-core](https://github.com/XTLS/Xray-core) binary for a Padavan router
(MediaTek MT7621, `linux/mipsle`, soft-float — the SoC has no FPU).

The router has 16MB of flash and no USB, so the binary cannot be stored on the
device: it lives in `/tmp` (RAM) and is re-downloaded from here after every reboot.

| | |
|---|---|
| Version | 26.7.28 |
| Source | official `Xray-linux-mips32le.zip` release asset, `xray_softfloat` |
| md5 (gzipped) | `515c31bd870da172ea1b477ce8c6b9ed` |
| md5 (unpacked) | `858ebbb5db3d159489fb39ba5ab58603` |

The router verifies the unpacked md5 before executing it.

> Note: Xray **26.3.27 crashes** on this router's 3.4.113 kernel (`futexwakeup … -89`,
> then SIGSEGV). Both older and newer builds are fine, so pin deliberately.
