---
description: 启用上次修改的响应标头。 启用或禁用在图像服务发出的可缓存HTTP响应中包含“上次修改时间”标头。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 2%

---

# UseLastModified{#uselastmodified}

启用上次修改的响应标头。 启用或禁用在图像服务发出的可缓存HTTP响应中包含“上次修改时间”标头。

服务器将响应中涉及的所有目录/目录记录的最近`catalog::TimeStamp`值用作上次修改的标头值。

仅当使用不支持etag标头的分布式缓存网络或其他缓存系统时，才应启用。

>[!NOTE]
>
>在涉及多个图像服务主机的负载平衡环境中使用上次修改时间标头时，必须小心。 如果由于某些原因，服务器对同一目录条目具有不同的时间戳，则客户端缓存可能会失败，服务器负载会增加。 这种情况可能发生如下：
>
>* 既不是`catalog::TimeStamp`也不是`attribute::TimeStamp`，因此[!DNL catalog.ini]文件的修改时间将用作`catalog::TimeStamp`的默认值。
   >
   >
* 每台服务器在本地文件系统上都有自己的目录文件实例，而不是通过网络装载来共享图像目录文件。
>* 同一[!DNL catalog.ini]文件的两个或多个实例具有不同的文件修改日期，这可能是由于文件复制不当所致。

>



## 属性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

标记. 0表示禁用，1表示启用上次修改的HTTP头。

## 默认 {#section-4eb47aadab8b41609bef296a4115f9f4}

从`default::UseLastModified`继承（如果未定义或为空）。

## 另请参阅 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
