---
description: 默认客户端缓存的活动时间。 提供默认的过期间隔，以防特定的目录记录不包含有效的目录过期值或晕影过期值，或者如果直接访问晕影文件或材料文件，而不是通过目录记录。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 3%

---


# 过期时间{#expiration}

默认客户端缓存的活动时间。 提供默认的过期时间间隔，以防特定目录记录不包含有效的目录：:Expiration或晕影：:Expiration值，或者如果直接访问晕影文件或材料文件，而不是通过目录记录。

## 属性 {#section-8e2bade105ec4905ae5c4911f500279f}

实数，0或更大。 自生成回复数据以来到期的小时数。 设置为0可始终立即使回复图像过期，这会有效地禁用客户端缓存。 设置为–1将标记为&#x200B;*永不过期*。

## 默认 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

从默认继承：：如果未定义或为空，则过期。

## 另请参阅 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [晕影：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
