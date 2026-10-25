# Hackintosh on Legion 15IRX10 (Sequoia)
A pre-built EFI file for **Legion 15IRX10**

Can be used as reference for simmilar devices for troubleshooting if needed.

## Summary Device Specs
- i7-13650HX
- RTX 5050m
- 16GB DDR5 SODIMM
- 512GB NVMe

## Status
Device extracted SSDT does not work, yoinked other simmilar device's EFI apperently worked.
| device | Status | Notes |
|-----|--------| ----------|
| `CPU` | ✅ | Working on all 8 cores (HT too) |
| `GPU` | ✅ | nullmoth's driver, stable enough to be used as daily, stutters on maxxed gaming settings |
| `SSD` | ✅ | both slots worked |
| `Speaker` | ✅ |  |
| `USB` | ✅ | |
| `3.5mm` | ⚠️ | Working, but the audio is muffled.|
| `Keyboard` | ✅ ||
| `Trackpad` | ❌ ||
| `Wifi` | ✅ |itlwm|
| `Bluetooth` | ✅ ||

## Device Quirks
- DisableIoMapper must set to `true`, otherwise it will panic.
- CpuTscSync is required due to prevent non-monotonic-time panic.

## Notes
The EFI file is still dirty due to a mixup with other simmilar device's.
AMFIPass only here due to nullmoth's driver