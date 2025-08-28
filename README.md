# FSTAB Fixer for EXT4/BTRFS 🐧🔧

<p align="center">
  <a href="https://github.com/LINUX-OASIS/FSTAB-FIXER/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-GPLv3-blue.svg?style=for-the-badge" alt="License: GPL v3">
  </a>
  <a href="https://github.com/LINUX-OASIS/FSTAB-FIXER/issues">
    <img src="https://img.shields.io/github/issues/LINUX-OASIS/FSTAB-FIXER?style=for-the-badge&logo=github&color=orange" alt="GitHub issues">
  </a>
  <a href="https://github.com/LINUX-OASIS/FSTAB-FIXER/pulls">
    <img src="https://img.shields.io/github/issues-pr/LINUX-OASIS/FSTAB-FIXER?style=for-the-badge&logo=github&color=green" alt="GitHub PRs">
  </a>
  <a href="https://github.com/LINUX-OASIS/FSTAB-FIXER/releases">
    <img src="https://img.shields.io/github/v/release/LINUX-OASIS/FSTAB-FIXER?style=for-the-badge&logo=github" alt="GitHub release">
  </a>
  <br>
  <img src="https://img.shields.io/badge/Shell_Script-121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white" alt="Made with Bash">
  <img src="https://img.shields.io/badge/OS-Linux-blue?style=for-the-badge&logo=linux&logoColor=white" alt="Runs on Linux">
  <img src="https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg?style=for-the-badge" alt="Contributions Welcome">
</p>

<p align="center">
  A safe, interactive TUI-based shell script to correct UUID entries in <code>/etc/fstab</code> for root (<code>/</code>) and EFI (<code>/boot/efi</code>) partitions. Perfect for post-cloning or migrating a Linux installation to a new drive!
</p>

---

<!-- Optional: Add a GIF of the script in action -->
<!-- <p align="center">
  <img src="https://raw.githubusercontent.com/LINUX-OASIS/FSTAB-FIXER/main/demo.gif" alt="FSTAB Fixer Demo">
</p> -->

## ✨ Features

* **Interactive TUI**: Utilizes `whiptail` to provide a clean, colorful, and easy-to-use terminal interface.
* **Safe & Non-Destructive**: Mounts filesystems to a temporary location and requires confirmation before writing any changes.
* **Smart Partition Detection**: Automatically lists available `ext4`/`btrfs` (for OS) and `vfat` (for EFI) partitions for easy selection.
* **BTRFS Subvolume Support**: Intelligently detects and allows you to select the correct BTRFS root subvolume.
* **Automatic Cleanup**: Guarantees that temporary mount points are unmounted and removed, even if the script is interrupted.
* **Zero Configuration**: No need to edit files or set variables. Just run it and follow the prompts.

## 🖥️ Compatibility

This script is designed to be broadly compatible with most modern Linux distributions. It has been primarily developed and tested on:

* **Debian**
* **Ubuntu**
* **Linux Mint**
* ...and other Debian/Ubuntu derivatives that use the `apt` package manager.

It should work on other distributions as well, provided the necessary dependencies are installed.

## ⚙️ Getting Started

### Prerequisites

The script relies on a few common system utilities. It will attempt to install any that are missing on `apt`-based systems.

* `whiptail` (from the `newt-tui` package)
* `btrfs-progs` (for BTRFS support)
* `util-linux` (provides `lsblk` and `blkid`)
* `sudo` (to perform privileged operations)

### Installation & Usage

1. **Clone the repository:**
    ```bash
    git clone https://github.com/LINUX-OASIS/FSTAB-FIXER.git
    cd FSTAB-FIXER
    ```

2. **Make the script executable:**
    ```bash
    chmod +x custom-FSTAB-FIXER.sh
    ```

3. **Run the script with `sudo`:**
    The script needs root privileges to mount partitions and edit the `fstab` file.
    ```bash
    sudo ./custom-FSTAB-FIXER.sh
    ```

Follow the on-screen prompts to select your new OS and EFI partitions, and the script will handle the rest!

---

## 💬 Contributing

Pull requests, issues, and suggestions are warmly welcomed! We believe in the power of community collaboration to make tools better.

See [CONTRIBUTING.md](https://github.com/LINUX-OASIS/FSTAB-FIXER/blob/main/CONTRIBUTING.md) for guidelines.

## 🌐 Links

* [Issues](https://github.com/LINUX-OASIS/FSTAB-FIXER/issues) — Report bugs or request features.
* [Pull Requests](https://github.com/LINUX-OASIS/FSTAB-FIXER/pulls) — Contribute your own fixes or improvements.
* [Releases](https://github.com/LINUX-OASIS/FSTAB-FIXER/releases) — Download stable versions.
* [Wiki](https://github.com/LINUX-OASIS/FSTAB-FIXER/wiki) — Find more in-depth documentation.

## 🧙‍♂️ Maintainer

This project is maintained by **[LINUX-OASIS](https://github.com/LINUX-OASIS)**.

## 📜 License

This project is licensed under the **GNU General Public License v3.0**. See the [LICENSE](https://github.com/LINUX-OASIS/FSTAB-FIXER/blob/main/LICENSE) file for details.
