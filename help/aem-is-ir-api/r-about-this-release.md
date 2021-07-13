---
description: 此版本（图像提供6.6.1和图像呈现6.6.1）取代了图像提供6.5.3和图像呈现6.5.3。
solution: Experience Manager
title: 关于此版本
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# 关于此版本{#about-this-release}

此版本（图像提供6.6.1和图像呈现6.6.1）取代了图像提供6.5.3和图像呈现6.5.3。

## 已知问题和行为更改 {#section-9dbc05206187477f926a78e8108a34e1}

* 不再支持在资产ID中使用问号字符，即使该字符已进行URL编码。
* 不再支持动态横幅`/xfl/flash/`请求，现在返回http 404错误代码。
* 不再支持W2P `/is/agm/`请求。
* 某些错误消息不再呈现在浏览器中。 因此，您需要查看跟踪日志以进行调试。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智能色板
* 智能裁剪

## 错误修复 {#section-58dff74d56f64edeadf8f8b97b7a4161}

* 修复了`\qc` RTF选项后跟空格导致请求无法呈现的问题。
