---
description: 启用上次修改的响应标头。 启用或禁用在图像渲染发出的可缓存HTTP响应中包含“上次修改时间”标头。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 2%

---


# UseLastModified{#uselastmodified}

启用上次修改的响应标头。 启用或禁用在图像渲染发出的可缓存HTTP响应中包含“上次修改时间”标头。

服务器使用响应中涉及的所有晕影和材料目录/目录记录的最新`vignette::TimeStamp`和`catalog::TimeStamp`值作为“上次修改时间”标头值。

仅当使用不支持etag头的分布式缓存网络（如Akamai）时才应启用。

>[!NOTE]
>
>在涉及多个图像服务/渲染主机的负载平衡环境中使用上次修改时，必须小心。 如果由于某种原因，服务器对同一目录条目具有不同的时间戳，则可能会失败客户端缓存并增加服务器负载。 这种情况可能发生如下：

* 既未定义`catalog::TimeStamp`、`vignette::TimeStamp`和`attribute::TimeStamp`，因此[!DNL catalog.ini]文件的修改时间用作`catalog::TimeStamp`的默认值。

* 每台服务器都有其自己的本地文件系统目录文件实例，而不是通过网络装载共享材料目录文件。
* 同一[!DNL catalog.ini]文件的两个或多个实例具有不同的文件修改日期，这可能是由于文件复制不当所致。

## 属性 {#section-453952244193452caccfaf7f601007c1}

标记. 0表示禁用，1表示启用上次修改的HTTP头。

## 默认 {#section-ec8fae847ca2421d8cdcde324e5a2d76}

如果未定义或为空，则从`default::UseLastModified`继承。

## 另请参阅 {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [晕影：:TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
