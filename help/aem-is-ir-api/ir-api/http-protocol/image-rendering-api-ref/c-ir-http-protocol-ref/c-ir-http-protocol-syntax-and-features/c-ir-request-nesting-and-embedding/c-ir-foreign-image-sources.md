---
description: 图像服务支持对外部HTTP和FTP服务器上的源图像的访问。
seo-description: 图像服务支持对外部HTTP和FTP服务器上的源图像的访问。
seo-title: 外来图像源
solution: Experience Manager
title: 外来图像源
uuid: 28a17400-4807-4e14-937a-80309be53d55
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# 外部图像源{#foreign-image-sources}

图像服务支持对外部HTTP和FTP服务器上的源图像的访问。

为`src=`或`mask=`命令指定外来URL;只需用大括号分隔整个嵌入的URL:

` …&src={ *[!DNL foreignUrl]*}&…`

允许使用完全绝对URL（如果设置了`attribute::AllowDirectUrls`）和相对于`attribute::RootUrl`的URL。 如果嵌入了绝对URL并且包含以下属性，则会发生错误：`AllowDirectUrls`为0，或者如果指定了相对URL且`attribute::RootUrl`为空。

服务器根据HTTP响应中包含的缓存头对外部图像进行缓存。
