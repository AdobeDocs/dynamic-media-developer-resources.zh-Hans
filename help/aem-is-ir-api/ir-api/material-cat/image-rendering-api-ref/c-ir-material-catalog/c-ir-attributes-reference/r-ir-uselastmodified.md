---
title: UseLastModified
description: 启用上次修改的响应标头。 启用或禁用在由图像渲染发出的可缓存HTTP响应中包含Last-Modified标头。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

启用上次修改的响应标头。 启用或禁用在由图像渲染发出的可缓存HTTP响应中包含Last-Modified标头。

服务器使用最新的 `vignette::TimeStamp` 和 `catalog::TimeStamp` 响应中涉及的所有晕影和材质目录/目录记录的值，作为Last-Modified标头值。

仅当使用不支持etag标头的分布式缓存网络（例如Akamai）时，才应启用。

>[!NOTE]
>
>在涉及多个图像服务/渲染主机的负载平衡环境中使用Last-Modified标头时，必须谨慎。 如果由于某些原因，服务器对于相同的目录条目具有不同的时间戳，则可能会挫败客户端缓存，并增加服务器负载。 这种情况可能发生在以下方面：

* `catalog::TimeStamp`， `vignette::TimeStamp`，或 `attribute::TimeStamp` 未定义，因此的修改时间 [!DNL catalog.ini] 文件用作的默认值 `catalog::TimeStamp`.

* 每个服务器在本地文件系统上都有自己的目录文件实例，而不是通过网络挂载共享材料目录文件。
* 同一实例的两个或多个实例 [!DNL catalog.ini] 文件具有不同的文件修改日期，可能是由于文件复制不当所致。

## 属性 {#section-453952244193452caccfaf7f601007c1}

标记. 0表示禁用，1表示启用上次修改的HTTP标头。

## 默认 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

继承自 `default::UseLastModified` 如果未定义或为空。

## 另请参阅 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog：：时间戳](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ， [晕影：：时间戳](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
