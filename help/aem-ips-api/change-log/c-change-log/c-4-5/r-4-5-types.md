---
description: 介绍IPS API版本4.5的新数据类型和更改的数据类型。
solution: Experience Manager
title: 新数据类型和修改的数据类型
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

---

# 数据类型：新增和已修改{#data-types-new-and-modified}

介绍IPS API版本4.5的新数据类型和更改的数据类型。

语法

## 新类型 {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## 已修改类型 {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* 资产包含新的 `fileName` 返回虚拟文件名的字段。
* `AssetSummary` 返回 `type` 和 `name` 字段

* `MetadataField` 包括 `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` 需要 `urlArray` 并添加一个可选 `numUrls` count
