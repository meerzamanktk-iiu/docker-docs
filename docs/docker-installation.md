# Docker Desktop Installation Guide

This guide will help you install Docker Desktop and resolve common setup issues.

---

## 1. Install Docker Desktop

Download and install Docker Desktop using the official installer:

https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe

Before starting the installation, review the official Docker documentation:

https://docs.docker.com/desktop/setup/install/windows-install/

Follow the installer instructions and complete the setup.

---

## 2. Fix "WSL Needs Updating" Error

After installing Docker Desktop, you may encounter the following error:

`WSL needs updating`

To resolve this issue:

1. Open **Command Prompt** as **Administrator**.
2. Run the following command:

```bash
wsl --update
```

3. This command updates the **Windows Subsystem for Linux (WSL)** on your system.

Once the update is complete, restart Docker Desktop.

---

## 3. Skip Docker Login

A Docker account is **not required** for this setup.

If Docker Desktop prompts you to sign in:
- Simply **skip the login step**.

If any issues occur:
- Follow **Step 2** to update WSL.
- Restart your system.

---

## ⚠️ System Requirements

> **Warning**
> Ensure your system meets the following requirements before installing Docker Desktop.  
> Docker may fail to start if these requirements are not satisfied.

Minimum requirements:

- **64-bit CPU with virtualization support enabled**
- **WSL 2 installed and enabled**
- **Windows 10 or Windows 11 (64-bit)**
- **Minimum 4 GB RAM (8 GB recommended)**

If virtualization is disabled, enable it in your **BIOS/UEFI settings** before installing Docker Desktop.
