Chapter 1 – Foundation
Week 1 – Session 1
Windows Subsystem for Linux (WSL) Installation – Ubuntu 24.04 LTS

This guide provides a complete, step-by-step setup for installing and configuring WSL (Windows Subsystem for Linux) with Ubuntu 24.04 LTS on Windows. It is designed for beginners starting their Linux, DevOps, AI/ML, or Software Development journey.

📌 Objective

Enable WSL on Windows

Install Ubuntu 24.04 LTS

Configure Linux user environment

Run Linux inside Windows

Prepare development-ready Linux environment


⚙️ Step 1 – Enable Windows Features

Open Control Panel

Navigate to:

Programs → Turn Windows features on or off


Enable the following:

✅ Virtual Machine Platform

✅ Windows Hypervisor Platform

✅ Windows Subsystem for Linux

Click OK

Restart your PC

⚙️ Step 2 – Install WSL

After restarting:

You can install WSL using Microsoft’s official command:

wsl --install


Or follow any trusted tutorial video:

Reference: WSL Installation Tutorial

This step installs:

WSL Kernel

Virtualization components

Default Linux environment

🔍 Step 3 – Verify WSL Installation

Open PowerShell and run:

wsl --version


Expected Output Example:

WSL version: 2.x.x
Kernel version: x.x.x


If version appears → ✅ WSL Installed Successfully

📦 Step 4 – List Available Linux Distributions

To see available Linux versions:

wsl --list --online


You will see options like:

Ubuntu

Ubuntu 22.04 LTS

Ubuntu 24.04 LTS

Debian

Kali Linux

openSUSE

🐧 Step 5 – Install Ubuntu 24.04 LTS

Run:

wsl --install ubuntu-24.04


This will:

Download Ubuntu

Install Linux filesystem

Set up WSL integration

⏳ Installation may take 5–15 minutes depending on internet speed.

👤 Step 6 – Create Linux User & Password

After installation completes, Ubuntu terminal will open and prompt:

Create default UNIX user account:


Enter username:
abdulraheem


Then set password:

New password:
Retype new password:


⚠️ Password will NOT be visible while typing (normal behavior).

🖥️ Step 7 – Use Ubuntu in Windows

Ubuntu is now fully installed 🎉

You can launch Ubuntu using:

Method 1 – Start Menu
Start → Search → Ubuntu → Open

Method 2 – PowerShell / Command Prompt
wsl

Method 3 – Direct Ubuntu Command
ubuntu

📂 Basic Linux Commands (Quick Start)
ls          # List files
pwd         # Show current directory
cd ~        # Go to home directory
whoami      # Show current user
sudo apt update
sudo apt upgrade

🔧 Update Ubuntu (Recommended)

After first launch, run:

sudo apt update && sudo apt upgrade -y


This updates:

Packages

Security patches

System components

🏗️ WSL Architecture
Windows OS
   │
   ├── WSL Kernel
   │
   ├── Virtual Machine Platform
   │
   └── Ubuntu Linux Environment
            │
            ├── Linux Commands
            ├── Package Manager (APT)
            └── Development Tools

🧪 Verification Checklist
Task	Status
Windows Features Enabled	✅
WSL Installed	✅
Ubuntu Installed	✅
Linux User Created	✅
Ubuntu Running	✅
🎯 Key Learnings

Understanding WSL architecture

Running Linux inside Windows

Linux user environment setup

Basic Linux commands

Preparing development environment

🚀 Next Steps

After completing this session, you can:

Install Git inside Ubuntu

Install Python / Node.js

Setup VS Code with WSL

Start DevOps / AI / ML environment

Install Docker on WSL

Learn Linux commands

🛠️ Troubleshooting
WSL command not recognized

Run PowerShell as Administrator:

wsl --install

Virtualization not enabled

Enable Virtualization Technology (VT-x / AMD-V) in BIOS.

Ubuntu not opening

Try:

wsl --set-default ubuntu-24.04
wsl

📚 Resources

Microsoft Official WSL Docs

Ubuntu Documentation

Linux Command Guide
Session: Week 1 – Session 1

📌 Session Status
✔ Session 1 Completed Successfully

I
