---
description: 启用上次修改的响应标头。 启用或禁用在由图像服务发出的可缓存HTTP响应中包含Last-Modified标头。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

启用上次修改的响应标头。 启用或禁用在由图像服务发出的可缓存HTTP响应中包含Last-Modified标头。

服务器使用最新的 `catalog::TimeStamp` 响应中涉及的所有目录/目录记录的值，作为Last-Modified标头值。

仅当使用的分布式缓存网络或其他缓存系统不支持etag标头时，才应启用。

>[!NOTE]
>
>在涉及多个图像服务主机的负载平衡环境中使用Last-Modified标头时，必须小心。 如果由于某些原因，服务器对于相同的目录条目具有不同的时间戳，则可能会挫败客户端缓存，并增加服务器负载。 这种情况可能发生在以下方面：
>
>* 两者都不是 `catalog::TimeStamp` 也不 `attribute::TimeStamp`，这样对的修改时间 [!DNL catalog.ini] 文件用作的默认值 `catalog::TimeStamp`.
>
>* 每个服务器在本地文件系统中都有自己的目录文件实例，而不是通过网络挂载共享映像目录文件。
>* 同一实例的两个或多个实例 [!DNL catalog.ini] 文件具有不同的文件修改日期，可能是由于文件复制不当所致。
>

## 属性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

标记. 0表示禁用，1表示启用上次修改的HTTP标头。

## 默认 {#section-4eb47aadab8b41609bef296a4115f9f4}

继承自 `default::UseLastModified` 如果未定义或为空。

## 另请参阅 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog：：时间戳](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
