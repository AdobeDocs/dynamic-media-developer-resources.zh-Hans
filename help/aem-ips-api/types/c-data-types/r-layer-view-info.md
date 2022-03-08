---
description: 层视图属性。
solution: Experience Manager
title: 层视图信息
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 12%

---

# 层视图信息{#layerviewinfo}

层视图属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| url | `xsd:string` | 表示模板的图像服务器URL。 组合 `urlModifier` 和 `urlPostAp- plyModifier` 字段。 |
| urlModifier | `xsd:string` | 在请求或 `urlPostApplyModifier` 中。 |
| urlPostApplyModifier | `xsd:string` | 要在之后应用的图像服务协议命令 `urlModifier` 和请求命令。 |
