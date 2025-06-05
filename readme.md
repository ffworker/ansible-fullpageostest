# FullPageOS Raspberry Pi Setup with Ansible + VNC Viewer

This repo allows you to automatically configure a Raspberry Pi running [FullPageOS](https://github.com/guysoft/FullPageOS) to:
- Update the OS
- Set a specific browser URL (via `/boot/fullpageos.txt`)
- Install and configure `x11vnc` to mirror the Pi’s **HDMI output** over VNC

## 🚀 Features

- No desktop environment is launched — VNC shows exactly what’s on the Pi's screen.
- Zero manual setup after flashing your SD card.
- Secure enough for local use (VNC is view-only with no password).
- Lightweight and minimal for signage, kiosk, or wall-mounted dashboards.

---

## 🔧 Manual Pre-Setup (Do Once Per Pi)

Before using the playbook:

1. **Boot FullPageOS** and connect via HDMI and Ethernet.
2. **Find the Pi's IP address** (via router or screen).
3. **SSH into it from your Ansible machine**:

    ```bash
    ssh pi@<pi-ip>
    ```

    Accept the SSH fingerprint prompt.

4. Ansible will automatically ensure required system packages are present.

---

## 📁 Project Structure
