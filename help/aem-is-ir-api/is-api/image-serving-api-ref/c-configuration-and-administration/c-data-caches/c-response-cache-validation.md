---
description: 使用属性CacheValidationPolicy（在default.ini中或特定图像目录的.ini文件中）选择的基于目录或基于过期的缓存验证自动刷新缓存条目。
solution: Experience Manager
title: 响应缓存验证
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---


# 响应缓存验证{#response-cache-validation}

使用属性：:CacheValidationPolicy（在default.ini中或特定图像目录的.ini文件中）选择的基于目录或基于过期的缓存验证自动刷新缓存条目。

通过基于目录的验证，如果`catalog::LastModified`（或`attribute::LastModified`，或[!DNL catalog.ini]文件的文件修改时间）比创建缓存条目时间更近，则现有缓存条目会被视为过时。

使用基于过期的验证，缓存条目在自最近的验证后5分钟后变得过时。 在这两种情况下，服务器通过检查与创建请求相关的所有图像文件的文件日期来验证过时的缓存条目。 如果文件日期未更改，则更新缓存条目的时间戳，并且缓存日期被视为有效。

对于通常涉及的图像目录中注册的图像较多的应用程序，基于目录的验证可提供性能优势。 不涉及图像目录的应用程序应使用基于过期的缓存验证。 实现此目的的一种方法是在[!DNL default.ini]中设置`attribute::cacheValidationPolicy=0`，在所有特定图像目录文件中设置`1`。

当请求中涉及的目录条目以可能导致回复图像更改的方式发生更改时，缓存条目将变为无效，并且可能会重新生成。 例如，`catalog::Modifier`的内容会更改。

>[!NOTE]
>
>Dynamic Media pyramid TIFF(PTIFF)图像会在文件标题中内部维护文件日期，以便进行验证。 文件系统维护的文件修改时间用于检查非PTIFF文件是否已更改。

只有图像文件参与缓存验证过程。 更改字体文件或ICC用户档案文件不会导致缓存条目自动失效。
