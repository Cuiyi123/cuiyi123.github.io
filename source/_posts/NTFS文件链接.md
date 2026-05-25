---
title: NTFS文件链接
categories: Windows
tags:
  - Windows
  - Symbolic Link
  - 符号链接
abbrlink: '1828'
date: 2020-09-05 13:50:31
---
创建符号链接（Symbolic Link）的方法是在目标文件夹下，复制路径，用命令行工具CMD中DIR命令，打开目标文件夹路径，再使用mklink命令工具。
Mklink LinkFileName.(txt) D:\Filename.txt
其中 LinkFileName.(txt) 为符号链接，D:\Filename.txt为源文件路径。
