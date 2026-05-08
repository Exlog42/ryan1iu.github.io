---
title: i3wm下使用libinput-gestures实现触控板手势
date: 2026-04-01
draft: false
tags: 水文
categories: 折腾
---

好久没发了，水一篇文章。

## 安装

首先安装libinput-gestures

```bash
sudo pacman -S xdotool wmctrl
yay -S libinput-gestures
```

启动

```bash
libinput-gestures-setup autostart start
```

## 配置

编辑配置文件：

```
~/.config/libinput-gestures.conf
```

我的配置示例：

```conf
gesture swipe up    3 xdotool key alt+Up
gesture swipe down  3 xdotool key alt+Down
gesture swipe left  3 xdotool key alt+Left
gesture swipe right 3 xdotool key alt+Right

gesture pinch in    2 xdotool key ctrl+minus
gesture pinch out   2 xdotool key ctrl+plus

gesture swipe left  4 xdotool key alt+shift+Tab
gesture swipe right 4 xdotool key alt+Tab
```

## 重启

```bash
libinput-gestures-setup restart
```
