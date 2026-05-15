# Xiaomi Bootloader Unlock Guide

This guide explains how to unlock the bootloader on a Xiaomi device you own.

> WARNING:
> Unlocking the bootloader will usually erase all data on the device.
> Back up important files before continuing.

---
# Miui
# Requirements

- Xiaomi phone
- Mi account
- Windows PC
- USB cable
- Internet connection
- Battery above 60%

---

# Enable Developer Options

1. Open **Settings**
2. Go to **About phone**
3. Tap **MIUI Version** or **OS Version** 7 times
4. You should see:
   ```
   You are now a developer
   ```

---

# Enable OEM Unlocking & USB Debugging

1. Open:
   ```
   Settings → Additional Settings → Developer Options
   ```

2. Enable:
   - OEM Unlocking
   - USB Debugging

3. Enable:
   - USB Debugging (Security Settings) if available

---

# Bind Mi Account To Device

1. Insert a SIM card
2. Enable mobile data
3. Go to:
   ```
   Settings → Additional Settings → Developer Options → Mi Unlock Status
   ```

4. Tap:
   ```
   Add account and device
   ```

5. Wait for:
   ```
   Added successfully
   ```

> IMPORTANT:
> Use mobile data during this step.

---

# Download Mi Unlock Tool

Official Xiaomi unlock tool:

https://en.miui.com/unlock/

Extract the ZIP file on your PC.

---

# Boot Into Fastboot Mode

Power off the phone.

Hold:

```text
Volume Down + Power
```

Until the Fastboot screen appears.

---

# Connect Device To PC

Use a USB cable and connect the device.

Verify connection:

```bash
fastboot devices
```

You should see your device serial number.

---

# Unlock Bootloader

1. Open:
   ```
   miflash_unlock.exe
   ```

2. Log in with the same Mi account used on the phone

3. Read warnings

4. Click:
   ```
   Unlock
   ```

---

# Waiting Period

Xiaomi may require a waiting period such as:

- 168 hours
- 360 hours

If required:

- Keep the Mi account logged in
- Do not remove the account
- Wait the required time
- Retry later

---

# Finish Unlock

After successful unlock:

```text
Unlocked successfully
```

The device will reboot and factory reset.

---

# Verify Bootloader Status

Enable USB debugging again after setup.

Run:

```bash
adb reboot bootloader
```

Then:

```bash
fastboot oem device-info
```

Look for:

```text
Device unlocked: true
```

---

# Globle HyperOS
# Requirements
- Xiaomi phone
- Mi account
- Windows PC
- USB cable
- Internet connection
- Battery above 60%
- Got unlocking access from Xiaomi community

---
# Unlocking access
1. Open Xiaomi community app
2. Go to myself and than press `Unlock Bootloader`
3. At 00:00 Chinese (GMT+8) time they will release 50 unlocking premission.
4. If you got one you can go to the nex step.
---
# Enable Developer Options

1. Open **Settings**
2. Go to **About phone**
3. Tap **Hyperos Version** or **OS Version** 7 times
4. You should see:
   ```
   You are now a developer
   ```
---
# Bind Mi Account To Device

1. Insert a SIM card
2. Enable mobile data
3. Go to:
   ```
   Settings → Additional Settings → Developer Options → Mi Unlock Status
   ```

4. Tap:
   ```
   Add account and device
   ```

5. Wait for:
   ```
   Added successfully
   ```

> IMPORTANT:
> Use mobile data during this step.

---

# Download Mi Unlock Tool

Official Xiaomi unlock tool:

https://en.miui.com/unlock/

Extract the ZIP file on your PC.

---

# Boot Into Fastboot Mode

Power off the phone.

Hold:

```text
Volume Down + Power
```

Until the Fastboot screen appears.

---

# Connect Device To PC

Use a USB cable and connect the device.

Verify connection:

```bash
fastboot devices
```

You should see your device serial number.

---

# Unlock Bootloader

1. Open:
   ```
   miflash_unlock.exe
   ```

2. Log in with the same Mi account used on the phone

3. Read warnings

4. Click:
   ```
   Unlock
   ```

---

# Waiting Period

Xiaomi may require a waiting period such as:

- 168 hours
- 360 hours

If required:

- Keep the Mi account logged in
- Do not remove the account
- Wait the required time
- Retry later

---

# Finish Unlock

After successful unlock:

```text
Unlocked successfully
```

The device will reboot and factory reset.

---


# Optional Next Steps

After unlocking you can:

- Install Magisk
- Flash custom recovery
- Install custom ROMs
- Root the device

---

# Common Problems

## Device Not Detected

Install Xiaomi USB drivers.

Try another USB port/cable.

---

## Couldn't Verify Device

- Use mobile data
- Re-add Mi account
- Disable VPN

---

## Unlock Tool Stuck At 99%

Usually means waiting period not finished.

---

# Disclaimer

This guide is intended only for devices you own or are authorized to modify.
Unlocking the bootloader may void warranties and reduce device security.
