---
description: 层视图属性。
solution: Experience Manager
title: 层视图信息
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 11%

---

# 层视图信息{#layerviewinfo}

层视图属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`url`*` | `xsd:string` | 表示模板的图像服务器URL。 组合了`urlModifier`和`urlPostAp- plyModifier`字段。 |
| `*`urlModifier`*` | `xsd:string` | 在请求或`urlPostApplyModifier`命令之前应用的图像服务协议命令。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 在`urlModifier`和请求命令之后应用的图像服务协议命令。 |
