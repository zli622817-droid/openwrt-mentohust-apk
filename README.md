# openwrt-mentohust-apk
mentohust锐捷验证插件，ipk版本在25版本以上的openwrt不再适用，于是编译出apk版（包含二进制程序与 LuCI 界面）。


---

## 📌 项目背景

由于 `mentohust` 锐捷验证插件的传统 `.ipk` 版本在 **25版本及以上** 的新版 OpenWrt 系统中不再适用，导致许多校园网同学升级系统后无法进行网络认证。

为了解决这一痛点，本项目特此编译了 **`.apk` 格式** 的版本，完美适配新版 OpenWrt 系统的软件包管理架构，帮助大家继续愉快地畅享校园网！

---

## ✨ 功能特点

* **双剑合璧**：同时提供底层内核程序与直观的 LuCI 网页后台控制面板。
* **完美兼容**：专门针对 OpenWrt 25+ 版本的 APK 包管理器进行优化。
* **稳定认证**：继承 MentoHUST 优秀的锐捷认证机制，断线自动重连。

---

## 🚀 下载与安装指南

### 1. 下载插件
前往本仓库右侧的 **[Releases (发行作品)](../../releases)** 页面，下载以下**两个** `.apk` 文件到你的电脑：
* `mentohust-0.3.1-r2.apk` （核心验证程序）
* `luci-app-mentohust-27.173.apk` （网页管理界面）

---

### 2. 命令行一键安装（推荐 💻）

使用 SSH 工具（如 Putty、Xshell 或终端）连接到你的 OpenWrt 路由器，将上述两个文件上传至路由器的 `/tmp` 目录下，然后**依次执行**以下命令进行安装：

```bash
apk add --allow-untrusted /tmp/mentohust-0.3.1-r2.apk
apk add --allow-untrusted /tmp/luci-app-mentohust-27.173.apk

3. 网页端安装方式（备选 🌐）

1. 登录你的 OpenWrt 后台（LuCI 管理界面）。
2. 导航至：系统 -> 软件包 (System -> Software)。
3. 点击 "上传软件包"，先上传并安装 mentohust-0.3.1-r2.apk。
4. 随后再次点击上传，安装 luci-app-mentohust-27.173.apk。

