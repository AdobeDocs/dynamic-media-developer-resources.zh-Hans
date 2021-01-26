---
description: 启用上次修改的响应标头。 启用或禁用在图像服务发出的可缓存HTTP响应中包含上次修改时间标头。
seo-description: 启用上次修改的响应标头。 启用或禁用在图像服务发出的可缓存HTTP响应中包含上次修改时间标头。
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# UseLastModified{#uselastmodified}

启用上次修改的响应标头。 启用或禁用在图像服务发出的可缓存HTTP响应中包含上次修改时间标头。

服务器使用响应中涉及的所有目录／目录记录的最近`catalog::TimeStamp`值作为“上次修改时间”标题值。

仅当使用不支持etag头的分布式缓存网络或其他缓存系统时，才应启用。

>[!NOTE]
>
>在涉及多个图像服务主机的负载平衡环境中使用上次修改时间的标头时，必须小心。 如果由于某种原因，服务器对同一目录条目具有不同的时间戳，则客户端缓存可能会失败并增加服务器负载。 这种情况可能发生如下：
>
>* `catalog::TimeStamp`和`attribute::TimeStamp`均不使用，因此[!DNL catalog.ini]文件的修改时间将用作`catalog::TimeStamp`的默认值。
   >
   >
* 每台服务器在本地文件系统上都有其自己的目录文件实例，而不是通过网络装载共享图像目录文件。
>* 同一[!DNL catalog.ini]文件的两个或多个实例具有不同的文件修改日期，这可能是由于文件复制不当所致。

>



## 属性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

标记. 0表示禁用，1表示启用上次修改的HTTP头。

## 默认 {#section-4eb47aadab8b41609bef296a4115f9f4}

如果未定义或为空，则从`default::UseLastModified`继承。

## 另请参阅 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
