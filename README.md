# Arch Linux GNOME 安装配置

用于 archinstall 的 GNOME 桌面安装配置：`user_configuration_gnome.json`。

## 预设配置

- GNOME 桌面、GDM 登录管理器。
- Linux 内核、GRUB 引导器、Plymouth 启动画面。
- 简体中文 UTF-8 环境、美国键盘布局、Asia/Shanghai 时区。
- 中国镜像源、multilib 仓库、5 路并行下载。
- NetworkManager、PipeWire、蓝牙、打印服务、firewalld。
- 中文字体、Fcitx5 中文输入法、Firefox、LibreOffice。

## 使用命令

在 Arch Linux 安装介质中联网后，以 root 身份执行：

```bash
curl -fL https://raw.githubusercontent.com/buffmio/arch-install-config/main/user_configuration_gnome.json -o user_configuration_gnome.json
archinstall --config user_configuration_gnome.json
```

载入后，在安装界面补充下方的磁盘、用户和显卡驱动设置，再开始安装。

## 安装前需要设置

- 磁盘分区：`Disk configuration` → `Partitioning`。
- 创建用户：`Authentication` → `User account` → `Add a user`。
- 显卡驱动：`Profile` → `Graphics driver`。

完成设置并核对配置后，选择 `Install` 开始安装。

配置文件的版本字段为 `4.4`，需使用兼容其格式的 archinstall 版本。
