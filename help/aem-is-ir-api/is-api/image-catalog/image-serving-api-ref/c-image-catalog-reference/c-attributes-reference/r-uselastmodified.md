---
description: 启用上次修改的响应标头。 启用或禁用在由图像服务发出的可缓存HTTP响应中包含Last-Modified标头。
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
TQID: 'https://experienceleague.adobe.com/jmwz9jThBnFtTZBRoI0kbKwoxf1MU7rn1CpKrSU4f04'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

启用上次修改的响应标头。 启用或禁用在由图像服务发出的可缓存HTTP响应中包含Last-Modified标头。

服务器使用响应中涉及的所有目录/目录记录的最新`catalog::TimeStamp`值作为Last-Modified标头值。

仅当使用的分布式缓存网络或其他缓存系统不支持etag标头时，才应启用。

>[!NOTE]
>
>在涉及多个图像服务主机的负载平衡环境中使用Last-Modified标头时，必须小心。 如果由于某些原因，服务器对于相同的目录条目具有不同的时间戳，则可能会挫败客户端缓存，并增加服务器负载。 这种情况可能发生在以下方面：
>
>* 既不是`catalog::TimeStamp`，也不是`attribute::TimeStamp`，因此[!DNL catalog.ini]文件的修改时间将用作`catalog::TimeStamp`的默认时间。
>
>* 每个服务器在本地文件系统中都有自己的目录文件实例，而不是通过网络挂载共享映像目录文件。
>* 同一[!DNL catalog.ini]文件的两个或更多实例具有不同的文件修改日期，这可能是由于不正确复制文件所致。
>

## 属性 {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

标志。 0表示禁用，1表示启用上次修改的HTTP标头。

## 默认 {#section-4eb47aadab8b41609bef296a4115f9f4}

如果未定义或为空，则从`default::UseLastModified`继承。

## 另请参阅 {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalog：：时间戳](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
