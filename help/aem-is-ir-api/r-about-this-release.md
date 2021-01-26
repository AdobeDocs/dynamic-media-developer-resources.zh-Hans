---
description: 此版本（图像服务6.6.1和图像渲染6.6.1）将取代图像服务6.5.3和图像渲染6.5.3。
seo-description: 此版本（图像服务6.6.1和图像渲染6.6.1）将取代图像服务6.5.3和图像渲染6.5.3。
seo-title: 关于此版本
solution: Experience Manager
title: 关于此版本
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 1%

---


# 关于此版本{#about-this-release}

此版本（图像服务6.6.1和图像渲染6.6.1）将取代图像服务6.5.3和图像渲染6.5.3。

## 已知问题和行为更改{#section-9dbc05206187477f926a78e8108a34e1}

* 资产ID中不再支持使用问号字符，即使该字符是URL编码的。
* 不再支持动态横幅`/xfl/flash/`请求，现在返回http 404错误代码。
* 不再支持W2P `/is/agm/`请求。
* 某些错误消息不再呈现到浏览器。 因此，您需要查看跟踪日志以进行调试。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智能色板
* 智能裁剪

## 错误修复{#section-58dff74d56f64edeadf8f8b97b7a4161}

* 修复了`\qc` RTF选项后跟空格导致请求无法呈现的问题。

