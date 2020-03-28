---
description: 启用上次修改时间的响应标题。 启用或禁用在由图像渲染发出的可缓存HTTP响应中包含上次修改时间的标题。
seo-description: 启用上次修改时间的响应标题。 启用或禁用在由图像渲染发出的可缓存HTTP响应中包含上次修改时间的标题。
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

启用上次修改时间的响应标题。 启用或禁用在由图像渲染发出的可缓存HTTP响应中包含上次修改时间的标题。

服务器使用响应中涉 `vignette::TimeStamp` 及的所 `catalog::TimeStamp` 有晕影和材料目录／目录记录的最新和值作为“上次修改时间”标题值。

仅当使用不支持etag头的分布式缓存网络（如Akamai）时，才应启用该功能。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>在涉及多个图像服务／渲染主机的负载平衡环境中使用上次修改时间的标题时，必须小心。 如果由于某种原因，服务器对同一目录条目具有不同的时间戳，则可能会打败客户端缓存并增加服务器负载。 这种情况可能发生如下：

* 既 `catalog::TimeStamp`不定 `vignette::TimeStamp`义也不定义， `attribute::TimeStamp` 因此文件的修改时间 [!DNL catalog.ini] 将用作默认值 `catalog::TimeStamp`。

* 每台服务器都有其自己的目录文件实例，而不是通过网络装载共享材料目录文件。
* 同一文件的两个或两个以上实例的 [!DNL catalog.ini] 文件修改日期不同，这可能是由于文件复制不当所致。

## 属性 {#section-453952244193452caccfaf7f601007c1}

标记. 0表示禁用，1表示启用上次修改的HTTP头。

## 默认 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

如果未定义 `default::UseLastModified` 或为空，则从中继承。

## 另请参阅 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
