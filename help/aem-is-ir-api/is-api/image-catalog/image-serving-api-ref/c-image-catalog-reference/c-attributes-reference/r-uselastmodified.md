---
description: 启用上次修改时间的响应标题。 启用或禁用在由图像服务发出的可缓存HTTP响应中包含“上次修改时间”标题。
seo-description: 启用上次修改时间的响应标题。 启用或禁用在由图像服务发出的可缓存HTTP响应中包含“上次修改时间”标题。
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

启用上次修改时间的响应标题。 启用或禁用在由图像服务发出的可缓存HTTP响应中包含“上次修改时间”标题。

服务器使用响应中 `catalog::TimeStamp` 涉及的所有目录／目录记录的最新值作为“上次修改时间”标题值。

仅当使用不支持标签头的分布式缓存网络或其他缓存系统时，才应启用该功能。

>[!NOTE]
>
>在涉及多个图像服务主机的负载平衡环境中使用上次修改时间的标题时，必须小心。 如果由于某种原因，服务器对同一目录条目具有不同的时间戳，则可能会打败客户端缓存并增加服务器负载。 这种情况可能发生如下：
>
>* 也 `catalog::TimeStamp` 不 `attribute::TimeStamp`会，这样文件的修改时间 [!DNL catalog.ini] 将用作默认值 `catalog::TimeStamp`。
   >
   >
* 每台服务器都有其自己的目录文件实例，而不是通过网络装载共享图像目录文件。
>* 同一文件的两个或两个以上实例的 [!DNL catalog.ini] 文件修改日期不同，这可能是由于文件复制不当所致。
>



## 属性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

标记. 0表示禁用，1表示启用上次修改的HTTP头。

## 默认 {#section-4eb47aadab8b41609bef296a4115f9f4}

如果未定义 `default::UseLastModified` 或为空，则从中继承。

## 另请参阅 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
