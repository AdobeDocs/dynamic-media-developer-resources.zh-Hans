---
description: 此发行版本（图像提供6.6.1和图像渲染6.6.1）取代图像提供6.5.3和图像渲染6.5.3。
solution: Experience Manager
title: 关于此版本
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---

# 关于此版本{#about-this-release}

此发行版本（图像提供6.6.1和图像渲染6.6.1）取代图像提供6.5.3和图像渲染6.5.3。

## 已知问题和行为更改 {#section-9dbc05206187477f926a78e8108a34e1}

* 不再支持在资产ID中使用问号字符，即使该字符已进行URL编码也是如此。
* 动态横幅 `/xfl/flash/` 请求不再受支持，现在会返回HTTP 404错误代码。
* W2P `/is/agm/` 不再支持请求。
* 一些错误消息不再呈现给浏览器。 因此，您需要查看要调试的跟踪日志。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智能色板
* 智能裁剪

## 错误修复 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* 修复了以下问题 `\qc` RTF选项后跟空格导致请求无法呈现。
