---
description: 使用基于目录或基于到期的缓存验证自动刷新缓存条目，如使用属性CacheValidationPolicy（在default.ini或特定图像目录的.ini文件中）选择的那样。
solution: Experience Manager
title: 响应缓存验证
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# 响应缓存验证{#response-cache-validation}

使用基于目录或基于到期的缓存验证自动刷新缓存条目，如使用attribute：：CacheValidationPolicy（在default.ini中或特定图像目录的.ini文件中）选择的那样。

使用基于目录的验证，如果`catalog::LastModified`（或`attribute::LastModified`，或者[!DNL catalog.ini]文件的文件修改时间）晚于创建缓存项的时间，则现有的缓存项被视为过时。

使用基于到期的验证，自最近验证以来，缓存条目在5分钟后会失效。 在这两种情况下，服务器都通过检查与创建请求相关的所有图像文件的文件日期来验证过时的缓存条目。 如果文件日期未发生更改，则会更新缓存条目的时间戳，并将缓存日期视为有效。

对于主要涉及在图像目录中注册的图像的典型应用程序，基于目录的验证可提供性能优势。 不涉及图像目录的应用程序应使用基于到期的缓存验证。 实现此目标的一种方法是在[!DNL default.ini]中设置`attribute::cacheValidationPolicy=0`，并在所有特定图像目录文件中设置`1`。

当请求中涉及的目录条目以可能导致回复图像更改的方式发生更改时，缓存条目将变为无效并需要重新生成。 例如，`catalog::Modifier`的内容已更改。

>[!NOTE]
>
>Dynamic Media金字塔TIFF(PTIFF)图像在文件标题中内部维护文件日期以进行验证。 文件系统维护的文件修改时间用于检查非PTIFF文件是否已更改。

只有映像文件参与缓存验证过程。 更改字体文件或ICC配置文件不会导致缓存条目自动失效。
