## Docker Desktop Installation Guide

### 1. Install Docker Desktop
Download and install Docker Desktop from the following link:

https://desktop.docker.com/win/main/amd64/Docker%20Desktop%20Installer.exe

Before installing, review the official system requirements:
https://docs.docker.com/desktop/setup/install/windows-install/

---

### 2. Fix "WSL needs updating" Error

After installing Docker Desktop, you may see the error:

`WSL needs updating`

To fix this:

1. Open **Command Prompt as Administrator**.
2. Run the following command:

```bash
wsl --update
```

3. This will update **Windows Subsystem for Linux (WSL)** on your system.

---

### 3. Skip Docker Login

We do not require a Docker account for this setup.

If Docker Desktop asks you to log in, simply **skip the login step**.

If you encounter any errors:
- Follow **Step 2** to update WSL.
- Restart your system.

---

### System Requirements for Docker Desktop

Ensure your system meets the following requirements:

- **64-bit CPU with virtualization support**
- **WSL 2**
- **Windows 10 or Windows 11 (64-bit)**
- **Minimum 4 GB RAM (8 GB recommended)**
