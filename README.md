# 🐧 PenguinOS 1.0
Welcome to the official repository for PenguinOS 1.0, a minimalist operating system designed to be the "Final OS" after a legacy of experimental builds. This project represents a shift toward a professional, cloud-integrated development workflow.

🚀 The Mission
The goal of PenguinOS is to move past the "Hello World" stage and create a functional, lightweight environment using a Hybrid Kernel approach. This version focuses on stability, modularity, and storage efficiency.

Zero-Bloat Workflow: All heavy compilation is handled via GitHub Actions to prevent local disk space exhaustion.

Minimalist Foundation: Based on a stripped-down Linux kernel and Buildroot to keep the final image under 20MB.

Legacy Integration: Leveraging technical lessons learned from previous projects like KailanOS-XP-1.0.

🛠️ Tech Stack
Core: Minimal Linux Kernel (custom Kconfig).

Userspace: BusyBox for multi-call binary utilities.

Build System: Buildroot integrated with GitHub Actions.

Testing: QEMU for Windows (portable).

📦 Project Structure
/.github/workflows/: Contains the YAML files that power our cloud-based build system.

/board/penguin/: Custom kernel and system configurations.

/init/: Custom boot scripts and the iconic ASCII Penguin logo.

🚦 Getting Started
Since this OS is built in the cloud, you don't need to install massive toolchains on your Dell Latitude or OMEN laptop.

Push Changes: Edit your code or config files directly on GitHub or via your local terminal.

Cloud Build: GitHub Actions automatically triggers a build on every push.

Download Artifacts: Grab the resulting bzImage and rootfs.ext2 from the "Actions" tab.

Run with QEMU:

Bash
qemu-system-x86_64 -kernel bzImage -hda rootfs.ext2 -append "root=/dev/sda console=ttyS0" -serial stdio
🐧 About the Developer
Developed by Kailan, a student and developer focused on low-level software, x86 Assembly, and kernel exploration.

“No more Recycle Bins full of failed OSes. Just one Penguin to rule them all.”
