---
description: 使用属性CacheValidationPolicy（在default.ini或特定图像目录的。ini文件中）选择的基于目录或基于过期的缓存验证自动刷新缓存条目。
seo-description: 使用属性CacheValidationPolicy（在default.ini或特定图像目录的。ini文件中）选择的基于目录或基于过期的缓存验证自动刷新缓存条目。
seo-title: 响应缓存验证
solution: Experience Manager
title: 响应缓存验证
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# 响应缓存验证{#response-cache-validation}

使用属性：:CacheValidationPolicy（在default.ini或特定图像目录的。ini文件中）选择的基于目录或基于过期的缓存验证自动刷新缓存条目。

如果`catalog::LastModified`（或`attribute::LastModified`，或[!DNL catalog.ini]文件的文件修改时间）比创建缓存条目的时间更近，则使用基于目录的验证会将现有缓存条目视为过时。

使用基于过期的验证，缓存条目自最近的验证起在5分钟后变得过时。 在这两种情况下，服务器通过检查与创建请求相关的所有图像文件的文件日期来验证过时的缓存条目。 如果文件日期未更改，则更新缓存条目的时间戳，并将缓存日期视为有效。

对于通常涉及的图像目录中注册的图像较多的应用程序，基于目录的验证可提供性能优势。 不涉及图像目录的应用程序应使用基于过期的缓存验证。 实现此目的的一种方法是在[!DNL default.ini]中设置`attribute::cacheValidationPolicy=0`，在所有特定图像目录文件中设置`1`。

缓存条目无效，当请求中涉及的目录条目发生更改时，可能会导致回复图像发生更改。 例如，`catalog::Modifier`的内容会发生变化。

>[!NOTE]
>
>Dynamic Media金字塔TIFF(PTIFF)图像会在文件头中内部维护文件日期，以进行验证。 文件系统所维护的文件修改时间用于检查非PTIFF文件是否已更改。

只有图像文件参与缓存验证过程。 对字体文件或ICC用户档案文件所做的更改不会导致缓存条目的自动失效。
