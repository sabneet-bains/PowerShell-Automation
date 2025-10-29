<div align="center"><a name="readme-top"></a>

# ⚙️ PowerShell Automation — System Provisioning × Optimization Toolkit

[![PowerShell](https://img.shields.io/badge/PowerShell-7.x-3068B7?logo=powershell&logoColor=white&labelColor=0d1117&style=flat)](https://learn.microsoft.com/powershell/)
[![Windows](https://img.shields.io/badge/Platform-Windows_10%2B-0078D7?logo=windows11&logoColor=white&labelColor=0d1117&style=flat)](#)
[![Automation](https://img.shields.io/badge/Domain-System_Automation-lightgrey?logo=terminal&logoColor=white&labelColor=0d1117&style=flat)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-2ECC71?labelColor=0d1117&style=flat)](https://choosealicense.com/licenses/mit/)

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/sabneet-bains/PowerShell-Automation)

**Automating the Windows environment for consistency and performance.**  
<sup>*A modular PowerShell suite for reproducible system provisioning, developer setup, and configuration tuning across Windows 10 and 11.*</sup>

</div>

> [!NOTE]  
> <sup>Part of the <b>Foundational & Academic</b> collection — engineered for reproducibility, maintainability, and transparent system control.</sup>


## 🧭 Table of Contents
- [Overview](#-overview)
- [Core Capabilities](#-core-capabilities)
- [Prerequisites](#-prerequisites)
- [Function Reference](#-function-reference)
- [Usage](#-usage)
- [Contributing](#-contributing)
- [Future Work](#-future-work)
- [Author](#-author)
- [License](#-license)


## 🧠 Overview
This repository centralizes **Windows automation scripts** for streamlined environment setup, configuration, and optimization.  
Each PowerShell function is written for **idempotency**, **clarity**, and **reusability**, ensuring reproducible workstation provisioning.

### 🧩 Key Objectives
- Rapid post-installation setup for clean Windows environments.  
- Reproducible configuration of developer and productivity tools.  
- One-command deployment of system-wide preferences and optimizations.  

> [!TIP]  
> Each module can be executed individually or chained through the main `WindowsConfigScript.ps1` entry point.

<div align="right">

[![Back to Top](https://img.shields.io/badge/-⫛_TO_TOP-0d1117?style=flat)](#readme-top)

</div>


## ⚙️ Core Capabilities

| ⚡ Category | 🔍 Description |
|:------------|:----------------|
| **System Setup** | Configures display scaling, clipboard sync, and power profiles for optimal usability. |
| **Personalization** | Applies wallpapers, themes, accent colors, and taskbar/start-menu layouts. |
| **Accessibility** | Adjusts cursor, input, and assistive preferences for accessibility compliance. |
| **Network & Security** | Tunes TCP parameters, applies DNS-level ad-blocking (AdGuard Home), and optimizes privacy. |
| **Developer Tools** | Installs IDEs, compilers, Git, and Python environments for coding workflows. |
| **Productivity Stack** | Installs Office, Zoom, Slack, Firefox, Grammarly, and PowerToys. |
| **Hardware Optimization** | Configures GPU utilities (NVIDIA, MSI Afterburner) and MATLAB integration. |

> [!NOTE]  
> Each section is modular — you can execute full automation or target only specific categories (e.g., *DeveloperTools*, *NetworkSecurity*).

<div align="right">

[![Back to Top](https://img.shields.io/badge/-⫛_TO_TOP-0d1117?style=flat)](#readme-top)

</div>


## 🧱 Prerequisites
````text
Windows 10 or later  
Administrative privileges  
winget package manager  
Stable internet connection
````

The script validates prerequisites automatically on launch.  
`winget` will be installed if not already present.

> [!IMPORTANT]  
> Always run the script in an **elevated PowerShell session** to allow registry edits, app installations, and system configuration changes.

<div align="right">

[![Back to Top](https://img.shields.io/badge/-⫛_TO_TOP-0d1117?style=flat)](#readme-top)

</div>


## 📜 Function Reference

### 🧩 System & Core
| Function | Description |
|:----------|:-------------|
| `Test-Admin` | Confirms administrative privileges before execution. |
| `Install-Winget` | Installs **winget** if unavailable. |
| `Test-Preqs` | Validates PowerShell version, network, and environment readiness. |

---

### ⚙️ Configuration Modules
| Function | Description |
|:----------|:-------------|
| `Set-DisplayScaling` | Adjusts DPI and scaling across monitors. |
| `Set-PowerPlan` | Configures balanced or performance energy profiles. |
| `Set-Clipboard` | Enables cloud clipboard sync. |
| `Set-Background` / `Set-Colors` / `Set-Lockscreen` | Applies wallpapers, accent colors, and lock screens. |
| `Set-StartMenu` / `Set-Taskbar` | Customizes Start layout and pinned apps. |
| `Set-Accessibility` / `Set-Mouse-Pointer` | Tweaks input and accessibility preferences. |
| `Set-Windows-Settings` / `Set-Network-Settings` | Applies system-wide registry, privacy, and DNS settings. |

---

### 💼 Application Setup
| Function | Description |
|:----------|:-------------|
| `Install-AdGuardHome` | Deploys local DNS-level ad-blocking. |
| `Install-Dev-Tools` | Installs VS Code, Git, Python, and compilers. |
| `Install-MATLAB` / `Install-GPU-Software` | Configures MATLAB integration and GPU utilities. |
| `Install-Productivity-Software` | Installs Office, Slack, Zoom, and PowerToys. |
| `Set-Terminal` | Applies custom profiles to Windows Terminal. |

> [!TIP]  
> Functions are designed for modular execution — you can call individual modules or chain them into a full setup routine.


<div align="right">

[![Back to Top](https://img.shields.io/badge/-⫛_TO_TOP-0d1117?style=flat)](#readme-top)

</div>


## 🚀 Usage
````powershell
# 1. Set execution policy
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

# 2. Run the full setup
.\WindowsConfigScript.ps1
````

To run only a specific module (e.g., *Personalization*):
````powershell
.\WindowsConfigScript.ps1 -RunMode Personalization
````

> [!TIP]  
> The script automatically checks administrative status, verifies dependencies, and logs all actions in `%TEMP%\SetupLog.txt`.

<div align="right">

[![Back to Top](https://img.shields.io/badge/-⫛_TO_TOP-0d1117?style=flat)](#readme-top)

</div>


## 🤝 Contributing
**Contributions welcome!**  
To maintain clarity and portability:

1. Open an issue to propose improvements or new functions.  
2. Follow PowerShell conventions (`CmdletBinding`, parameter validation, error trapping).  
3. Add comments describing purpose, parameters, and expected behavior.  
4. Submit a pull request with **example output logs** for testing validation.

> [!TIP]  
> Ideal contributions include **automation profiles**, **GUI extensions**, and **cross-platform compatibility layers**.

<div align="right">

[![Back to Top](https://img.shields.io/badge/-⫛_TO_TOP-0d1117?style=flat)](#readme-top)

</div>


## 🔮 Future Work
- Develop a **GUI front-end** for easier task selection.  
- Extend GPU configuration to support **AMD ROCm** and Intel Arc.  
- Integrate **Ansible / DSC** for enterprise rollout.  
- Add **Pester-based CI tests** for consistency validation.  
- Implement **PowerShell logging dashboard** for real-time execution feedback.

<div align="right">

[![Back to Top](https://img.shields.io/badge/-⫛_TO_TOP-0d1117?style=flat)](#readme-top)

</div>


<div align="center">

##
### 👤 Author  
**Sabneet Bains**  
*Quantum × AI × Scientific Computing*  
[LinkedIn](https://www.linkedin.com/in/sabneet-bains/) • [GitHub](https://github.com/sabneet-bains)

##
### 📄 License  
Licensed under the [MIT License](https://choosealicense.com/licenses/mit/)

<sub>“Automation turns configuration into orchestration — precision at the command line.”</sub>

</div>
