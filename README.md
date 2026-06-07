# TB375FC prebuilt kernel - LineageOS 23.2

Prebuilt kernel for the Lenovo Xiaoxin Pad Pro 12.7 (2025), `TB375FC`
(MediaTek Dimensity 8300 / MT6897), as used by the LineageOS 23.2 (Android 16)
device tree.

## Contents

| Path | Description |
|------|-------------|
| `Image.gz` | gzip-compressed arm64 kernel image |
| `modules/` | kernel modules (`.ko`) plus the `system_dlkm` / `vendor_dlkm` / `vendor_ramdisk` load-order lists |
| `kernel-uapi-headers.tar.gz` | exported UAPI headers |

## Image

```
Linux version 6.1.173-android14-11-g2cb2e678e9eb
Android clang 17.0.2 (r487747c), LLD 17.0.2
```

6.1 GKI kernel on the `android14-11` KMI. MT6897 device-specific drivers that
have no published source ship as stock `.ko`; KMI stability lets them load
against this Image.

## Use

The device tree (`android_device_lenovo_TB375FC`) consumes this as a prebuilt
via `TARGET_PREBUILT_KERNEL`, so there is no kernel source to clone to build
the ROM.
