# Enterprise Linux Community Kernel Archives

**ELCKA** provides pre-built RPM packages of third-party Linux kernels for Linux distributions that use RPM as their package format, such as Fedora, CentOS, RHEL, and openSUSE. Instead of maintaining a full package repository, ELCKA offers direct downloads of standalone RPM files for manual installation via the `rpm` command.

---

## Available Kernels

### 1. **XanMod Kernel**
- **Website**: [https://xanmod.org](https://xanmod.org)
- **Description**: A custom Linux kernel optimized for desktop, gaming, and multimedia applications. The XanMod kernel includes performance enhancements to improve system responsiveness, reduce latency, and boost overall performance. It offers both **mainline** and **Real-Time (RT)** variants for different use cases.

### 2. **XanMod-RT Kernel**
- **Website**: [https://xanmod.org](https://xanmod.org)
- **Description**: The Real-Time variant of the XanMod kernel, designed for ultra-low latency use cases such as audio production, live streaming, and real-time applications. It provides the lowest possible latency, making it ideal for demanding, time-sensitive tasks.

### 3. **Linux-Zen Kernel**
- **Website**: [https://github.com/zen-kernel/zen-kernel](https://github.com/zen-kernel/zen-kernel)
- **Description**: The Zen Kernel is a community-driven project focused on balancing performance, stability, and hardware support. It incorporates various patches to improve desktop and gaming performance, providing a smoother and more responsive experience.

---

## Installation Instructions

### Download the RPM Packages
1. Visit the [Releases](https://github.com/Zhoneym/ELCKA/releases) section.
2. Download the appropriate RPM files for your desired kernel version. Example files include:
   - `kernel-6.12.18_rt_x64v3_xanmod1-1.x86_64.rpm` (Main kernel)
   - `kernel-headers-6.12.18_rt_x64v3_xanmod1-1.x86_64.rpm` (Kernel headers)
   - `kernel-devel-6.12.18_rt_x64v3_xanmod1-1.x86_64.rpm` (Development files)
   - `kernel-6.12.18_rt_x64v3_xanmod1-1.src.rpm` (Source code)

### Install the RPM Packages
To manually install the kernel packages, use the following commands:

```bash
# Install the main kernel
sudo rpm -ivh kernel-*.rpm

# Install the kernel development files
sudo rpm -ivh kernel-devel-*.rpm

# Install or update the kernel headers (use --replacepkgs if updating)
sudo rpm -Uvh --replacepkgs kernel-headers-*.rpm
```
