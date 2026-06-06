---
title: 在Windows-10操作系统中，如何系统级阻止某软件组件程序的运行？
categories:
  - 计算机
  - 计算机操作系统
  - 软件运行权限
tags:
  - Windows 10
  - 软件运行权限设置与阻止
abbrlink: 2cea
date: 2026-06-06 14:17:45
---

腾讯电脑管家软件，作为中国大陆一款流行的且强大的常规杀毒软件，很多人包括我在内，都使用了好多年了。

近几年，此款软件发布了好几个新版本。但是，令人难以置信的是，在这几款新版本内，软件居然在未征得用户明确的示意下，强行静默地安装了一些预先配置的组件程序，包括本地文件搜索工具、全局搜程序。

由于担心本地电脑隐私泄露及强行卸载其组件（本地文件搜索工具、全局搜程序）未果，不禁提出一个有待解决的问题：在Windows 10操作系统中，如何系统级阻止某软件组件程序的运行？

当然，现在具体的需求就是在本地电脑上，如何系统级阻止腾讯电脑管家软件，本地文件搜索工具、全局搜程序，这2个组件程序的运行？

## 定位此软件下组件核心搜索程序文件路径

首先需要定位【腾讯电脑管家】软件的安装目录。例如，安装目录是：

G:\Program Files\Tencent\QQPCMgr\18.2.30604.301

G:\Program Files\Tencent\QQPCMgr\18.2.30604.301\Qt64

找到以下3个核心搜索程序：

QMFileSearchApp.exe

QMLauncherEntrance64.exe

QMFileSearchProxy64.exe

* * *

## 方法一（步骤一）：注册表 IFEO 拦截（让程序启动即崩溃）

此方法无需删除文件，直接让系统拒绝执行它们。

1. `Win + R` → 输入 `regedit` → 回车

2. 定位到：
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options

3. 右键 → 新建 **项**，命名为 `QMFileSearchApp64.exe`

4. 在该项右侧，新建 **字符串值**，命名为 `Debugger`

5. 双击 `Debugger`，数值数据填入一个不存在的路径，例如：
    C:\Windows\System32\NonExistent.exe

6. 对 `QMLauncherEntrance64.exe` 重复步骤 3-5

**原理**：Windows 启动程序前会检查 IFEO 注册表。如果发现有 Debugger 指向，会先尝试启动"调试器"而非原程序。由于指向的程序不存在，原程序直接启动失败。

* * *

## Windows 10 家庭版如何启用组策略

Windows 10 家庭版默认不支持组策略编辑器（`gpedit.msc`），但可以通过以下方法手动启用。以下步骤适用于系统文件完整且无损坏的环境。

直接命令行启用

* **打开命令提示符** 以管理员身份运行 cmd。

* **执行以下命令**：

```batch
FOR %F IN ("%SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~*.mum") DO (DISM /Online /NoRestart /Add-Package:"%F")
FOR %F IN ("%SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~*.mum") DO (DISM /Online /NoRestart /Add-Package:"%F")
```

注意事项

* 如果仍无法启用，可以尝试第三方工具如 **Policy Plus**（[GitHub](https://github.com/Fleex255/PolicyPlus/releases/) 提供下载）。

* 执行操作前建议备份系统数据，以防意外。

* 部分功能可能受限于家庭版的系统架构。

通过以上方法，即可在 Windows 10 家庭版中成功启用组策略编辑器。

## 方法二（步骤二）：软件限制策略（系统级阻止）

1. `Win + R` → `gpedit.msc`（家庭版可能无此功能，需预先启用，参考上方。）
2. 计算机配置 → Windows 设置 → 安全设置 → **软件限制策略**
3. 右键"软件限制策略" → **创建新策略**
4. 左侧展开后，右键**其他规则** → **新建路径规则**
5. 浏览选择 `QMLauncherEntrance64.exe` (这个是全局搜组件程序)，安全级别设为**不允许**。
6. 同样添加 `QMFileSearchApp.exe`、`QMFileSearchApp64.exe`。

## 小结

通过方法一和方法二的两种办法的结合使用，双重限制阻止这些程序的运行，尽量保证操作的成功。

毕竟，腾讯电脑管家软件作为杀毒软件，核心进程很早就启动了，很难使用一般的方法卸载或删除其下的核心组件。

* * *

参考来源：Bing 搜索 & AI 类软件助手

* * *

*本文章仅供个人学习、参考。*
