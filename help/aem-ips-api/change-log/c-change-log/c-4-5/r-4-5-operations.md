---
description: 介绍IPS API版本4.5中新增和更改的操作方法。
solution: Experience Manager
title: 操作 — 新建和已修改
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
TQID: 'https://experienceleague.adobe.com/n4U8LW8otIaBBDalW1wRJFaweTAw3-0Sh0ckgIEADAI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 1%

---

# 操作：新建和已修改{#operations-new-and-modified}

介绍IPS API版本4.5中新增和更改的操作方法。

语法

## 新操作 {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## 已修改的操作 {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset`包括`animatedGifInfo`、`swcInfo`、`cssInfo`和`javascriptInfo`参数。
* `createMetadataField`包含可选的`isHidden`参数。
* `saveMetadataField`包含可选的`isHidden`参数。
* `searchAssets`
* `renameFiles`参数在以前的版本中已弃用，已从`renameAsset`操作中删除。 虚拟文件路径将更改以匹配新的资源名称（保留文件扩展名），而物理文件路径不受影响。 在更新到新的API版本时，API客户端需要移除对此参数的引用。
