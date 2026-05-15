# Android Rooting Guide (For Devices You Own)

This repository explains the basics of gaining root access on your own Android device for development, customization, and research purposes.

> WARNING:
> Unlocking the bootloader and rooting may void warranties, erase data, break banking apps, or reduce device security.

---

# What Is Root?

Root access gives administrative control over Android.

Common uses include:

- Installing custom ROMs
- Running advanced backup tools
- Removing bloatware
- Using system-level customization apps
- Development and testing

---

# Requirements

- Android device
- USB cable
- Computer with ADB and Fastboot installed
- Unlocked bootloader
- Device-specific firmware files
- Best if battery charged above 60%
- Devices boot.img or init_boot.img (use init_boot.img if it is present over boot.img)

---

# Install Platform Tools

Download Android platform tools:

https://developer.android.com/tools/releases/platform-tools

Verify installation:

```bash
adb version
fastboot --version
```

---

# Enable Developer Options

On the device:

1. Open Settings
2. About Phone
3. Tap "Build Number" 7 times
4. Enable:
   - USB Debugging
   - OEM Unlocking

---

# Unlock Bootloader (This is a generic guide go to company specific guide if this doesn't work)

> This usually wipes all data.

Reboot into bootloader:

```bash
adb reboot bootloader
```

Unlock:

```bash
fastboot flashing unlock
```

Some manufacturers use:

```bash
fastboot oem unlock
```

Follow on-screen confirmation.

---

# Root with Magisk Manager

1. Download stock firmware for your exact device model
2. Extract `boot.img` or `init_boot.img` (use init_boot.img if it is present over boot.img)
3. Install Magisk app on the phone
4. Patch the boot image in Magisk
5. Transfer patched image back to computer

---

# Flash Patched Boot Image (This work in basically all deives.)

Reboot into bootloader:

```bash
adb reboot bootloader
```

Flash patched image:

```bash
fastboot flash boot magisk_patched.img
```

Reboot:

```bash
fastboot reboot
```

---

# Verify Root

After reboot:

- Open Magisk or other root manager
- Verify superuser access

---

# Common Commands

Check device:

```bash
adb devices
```

Boot temporary image:

```bash
fastboot boot boot.img
```

Flash recovery:

```bash
fastboot flash recovery recovery.img
```

---

# Troubleshooting

## Device Not Detected

```bash
adb kill-server
adb start-server
```

## Bootloop

- Reflash original boot image
- Boot into recovery
- Factory reset if necessary

## Fastboot Waiting for Device

- Install USB drivers
- Change USB cable/port

---

# Safety Notes

- Only flash files made for your exact model
- Keep backups before modifying partitions
- Rooting can weaken device security
- Some apps may refuse to run on rooted devices

---

# Useful Tools

- ADB / Fastboot
- Magisk
- TWRP Recovery
- OEM USB Drivers

---

# Disclaimer

This repository is intended only for devices you own or are authorized to modify.

Do not use rooting techniques to bypass security, access unauthorized data, or violate laws or terms of service.
