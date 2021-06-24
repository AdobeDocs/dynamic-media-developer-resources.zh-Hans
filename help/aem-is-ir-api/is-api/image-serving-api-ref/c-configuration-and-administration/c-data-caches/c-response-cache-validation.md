---
description: 使用基于目录或基于过期的缓存验证自动刷新缓存条目，这与属性CacheValidationPolicy（在默认.ini或特定图像目录的.ini文件中）一起选择。
solution: Experience Manager
title: 响应缓存验证
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 响应缓存验证{#response-cache-validation}

使用基于目录或基于过期的缓存验证自动刷新缓存条目，这与属性：:CacheValidationPolicy（在默认.ini或特定图像目录的.ini文件中）一起选择。

通过基于目录的验证，如果`catalog::LastModified`（或`attribute::LastModified`，或[!DNL catalog.ini]文件的文件修改时间）比创建缓存条目时间更近，则现有缓存条目会被视为失效。

如果进行基于过期的验证，则自最近的验证后5分钟后，缓存条目会变为失效。 在这两种情况下，服务器都会通过检查与创建请求相关的所有图像文件的文件日期来验证过时的缓存条目。 如果文件日期未更改，则更新缓存条目的时间戳，并将缓存日期视为有效。

对于通常涉及的图像目录中注册的图像较多的应用程序，基于目录的验证可提供性能优势。 不涉及图像目录的应用程序应使用基于过期时间的缓存验证。 实现此目的的一种方法是在[!DNL default.ini]中设置`attribute::cacheValidationPolicy=0`，并在所有特定图像目录文件中设置`1`。

缓存条目将变为无效，如果请求中涉及的目录条目发生更改，而更改的方式可能会导致回复图像发生更改，则可能会重新生成缓存条目。 例如，`catalog::Modifier`的内容会发生更改。

>[!NOTE]
>
>Dynamic Media Pyramid TIFF(PTIFF)图像会出于验证目的在文件标题中内部维护文件日期。 文件系统维护的文件修改时间用于检查非PTIFF文件是否已更改。

只有图像文件参与缓存验证过程。 更改字体文件或ICC配置文件不会导致缓存条目自动失效。
