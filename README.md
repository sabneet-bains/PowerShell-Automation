# ⚙️ PowerShell Automation Repository  

[![PowerShell](https://img.shields.io/badge/PowerShell-7.x-blue?logo=powershell&logoColor=white)](https://learn.microsoft.com/powershell/)
[![Windows](https://img.shields.io/badge/Platform-Windows_10%2B-lightgrey?logo=windows11&logoColor=white)](#)
[![Automation](https://img.shields.io/badge/Domain-System_Automation-green)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://choosealicense.com/licenses/mit/)

<br>

**A collection of PowerShell scripts for automated Windows configuration, provisioning, and optimization.**  

This project centralizes environment setup tasks—system settings, personalization, software installation, and developer tool configuration—into a single reproducible script.


## 🧭 Table of Contents
- [Overview](#overview)
- [Core Capabilities](#core-capabilities)
- [Prerequisites](#prerequisites)
- [Function Reference](#function-reference)
- [Usage](#usage)
- [Contributing](#contributing)
- [Future Work](#future-work)
- [Author](#author)
- [License](#license)


## 🧩 Overview

This repository provides a **Windows automation script** designed for clean installations, reproducible workstation setup, and large-scale environment provisioning.  
It automates:

- Display scaling and power plan configuration.  
- Clipboard, background, color, and personalization settings.  
- Start menu, taskbar, and accessibility options.  
- Video playback and regional/time settings.  
- Developer tool and productivity software installation.  
- Network tuning and privacy optimizations.  

Each function is modular and can be invoked independently or as part of a full system setup routine.


## ⚙️ Core Capabilities

| Category | Description |
|-----------|-------------|
| **System Setup** | Configures display scaling, clipboard sync, power plans, and energy profiles. |
| **Personalization** | Sets background, accent colors, Start menu, lock screen, and taskbar preferences. |
| **Accessibility** | Adjusts cursor visibility, input methods, and assistive settings. |
| **Network & Security** | Tunes TCP parameters, installs AdGuard Home for ad-blocking DNS. |
| **Developer Tools** | Installs IDEs, Git utilities, compiler toolchains, and Python environments. |
| **Productivity Stack** | Installs Office, Grammarly, Zoom, Firefox, Slack, and PowerToys. |
| **Hardware Optimization** | Configures GPU software (NVIDIA, MSI Afterburner) and MATLAB support. |


## 🧱 Prerequisites

- **Windows 10 or later**  
- **Administrative privileges**  
- **`winget`** package manager (the script checks and installs if missing).  
- Internet connection for package installation and wallpaper retrieval.


## 📜 Function Reference

<details>
<summary>Click to expand function list</summary>

### System and Core
- `Test-Admin` — Ensures administrative privileges.  
- `Install-Winget` — Installs `winget` if unavailable.  
- `Test-Preqs` — Validates environment prerequisites.  

### Configuration
- `Set-DisplayScaling`, `Set-PowerPlan`, `Set-Clipboard` — System tuning.  
- `Set-Background`, `Set-Colors`, `Set-Lockscreen` — Visual customization.  
- `Set-StartMenu`, `Set-Taskbar`, `Set-Personalization` — UI layout optimization.  
- `Set-Accessibility`, `Set-Mouse-Pointer` — Accessibility configuration.  
- `Set-Windows-Settings`, `Set-Network-Settings` — System-wide preferences.  

### Application Setup
- `Install-AdGuardHome` — Installs DNS-level ad-blocker.  
- `Install-Dev-Tools` — Installs developer tools and languages.  
- `Install-MATLAB`, `Install-GPU-Software` — Scientific and GPU stack.  
- `Install-Productivity-Software` — Installs productivity apps.  
- `Set-Terminal` — Applies custom terminal profiles.

</details>


## 🚀 Usage

Run the script in an **elevated PowerShell session**:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
.\WindowsConfigScript.ps1
```

To execute specific modules (e.g., personalization only):

```powershell
.\WindowsConfigScript.ps1 -RunMode Personalization
```

> 💡 *The script will automatically check administrative status, install `winget` if missing, and continue configuration.*


## 🤝 Contributing

1. Open an issue to propose improvements or new functions.  
2. Follow PowerShell scripting best practices — `CmdletBinding`, parameter validation, and clear inline documentation.  
3. Submit a pull request with descriptive commit messages and example outputs.


## 🔮 Future Work

- Add a GUI-based PowerShell front-end for non-technical users.  
- Extend GPU configuration to support AMD ROCm environments.  
- Integrate with Ansible or DSC for enterprise deployment.  
- Add CI tests using **Pester** to validate script consistency.


## 👤 Author

**Sabneet Bains** — *Quantum × AI × Scientific Computing*  
[LinkedIn](https://www.linkedin.com/in/sabneet-bains/) • [GitHub](https://github.com/sabneet-bains)


## 📄 License

Licensed under the [MIT License](https://choosealicense.com/licenses/mit/).

