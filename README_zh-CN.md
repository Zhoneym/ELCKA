# Enterprise Linux Community Kernel Archives

**[简体中文 (Simplified Chinese)](README_zh-CN.md)** | [English](README.md)


**ELCKA** 提供预构建的第三方Linux内核的RPM包，适用于以RPM作为软件包格式的Linux发行版，如 Fedora、CentOS、RHEL 和 openSUSE。ELCKA 不维护完整的包仓库，而是通过直接下载独立的RPM文件，供用户通过 `rpm` 命令手动安装。

---

## 可用内核

### 1. **XanMod 内核**
- **官网**: [https://xanmod.org](https://xanmod.org)
- **描述**: XanMod 内核是为桌面、游戏和多媒体应用优化的自定义 Linux 内核。XanMod 内核包括性能优化，以提高系统响应能力、降低延迟并增强整体性能。它提供了 **主线** 和 **实时 (RT)** 两种变体，适用于不同的使用场景。

### 2. **XanMod-RT 内核**
- **官网**: [https://xanmod.org](https://xanmod.org)
- **描述**: XanMod 的实时变体，专为超低延迟的应用场景设计，例如音频制作、直播和实时应用。它提供最低的延迟，适合要求严格的时间敏感任务。

### 3. **Linux-Zen 内核**
- **官网**: [https://github.com/zen-kernel/zen-kernel](https://github.com/zen-kernel/zen-kernel)
- **描述**: Zen 内核是一个由社区驱动的项目，重点在于平衡性能、稳定性和硬件支持。它融合了多个补丁，旨在提升桌面和游戏性能，带来更流畅、更响应的体验。

---

## 安装说明

### 下载 RPM 包
1. 访问 [发布页面](https://github.com/Zhoneym/ELCKA/releases)。
2. 下载适合您所需内核版本的 RPM 文件。例如：
   - `kernel-6.12.18_rt_x64v3_xanmod1-1.x86_64.rpm` （主内核）
   - `kernel-headers-6.12.18_rt_x64v3_xanmod1-1.x86_64.rpm` （内核头文件）
   - `kernel-devel-6.12.18_rt_x64v3_xanmod1-1.x86_64.rpm` （开发文件）
   - `kernel-6.12.18_rt_x64v3_xanmod1-1.src.rpm` （源代码）

### 安装 RPM 包
要手动安装内核包，请使用以下命令：

```bash
# 安装主内核
sudo rpm -ivh kernel-*.rpm

# 安装内核开发文件
sudo rpm -ivh kernel-devel-*.rpm

# 安装或更新内核头文件
sudo rpm -Uvh --replacepkgs kernel-headers-*.rpm
```
