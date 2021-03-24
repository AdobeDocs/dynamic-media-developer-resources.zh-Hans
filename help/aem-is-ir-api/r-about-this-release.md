---
description: 此版本（图像服务6.6.1和图像渲染6.6.1）将取代图像服务6.5.3和图像渲染6.5.3。
solution: Experience Manager
title: 关于此版本
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# 关于此版本{#about-this-release}

此版本（图像服务6.6.1和图像渲染6.6.1）将取代图像服务6.5.3和图像渲染6.5.3。

## 已知问题和行为更改{#section-9dbc05206187477f926a78e8108a34e1}

* 不再支持在资产ID中使用问号字符，即使该字符是URL编码的。
* 不再支持动态横幅`/xfl/flash/`请求，现在返回http 404错误代码。
* 不再支持W2P `/is/agm/`请求。
* 某些错误消息不再呈现到浏览器。 因此，您需要查看要调试的跟踪日志。

## 新功能 {#section-b1386e36cb4544ebb79766a06b16842d}

* 智能色板
* 智能裁剪

## 错误修复{#section-58dff74d56f64edeadf8f8b97b7a4161}

* 修复了`\qc` RTF选项后跟空格导致请求未呈现的问题。

