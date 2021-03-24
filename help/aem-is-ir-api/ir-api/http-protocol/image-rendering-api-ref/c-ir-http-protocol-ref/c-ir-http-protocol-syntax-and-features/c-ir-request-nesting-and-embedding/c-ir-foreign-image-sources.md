---
description: 图像服务支持对外部HTTP和FTP服务器上的源图像的访问。
solution: Experience Manager
title: 外来图像源
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---


# 外部图像源{#foreign-image-sources}

图像服务支持对外部HTTP和FTP服务器上的源图像的访问。

为`src=`或`mask=`命令指定外来URL;只需用大括号分隔整个嵌入的URL:

` …&src={ *[!DNL foreignUrl]*}&…`

允许使用完全绝对URL（如果设置了`attribute::AllowDirectUrls`）和相对于`attribute::RootUrl`的URL。 如果嵌入了绝对URL并且包含以下属性，则会发生错误：`AllowDirectUrls`为0，或者如果指定了相对URL且`attribute::RootUrl`为空。

服务器根据HTTP响应中包含的缓存头对外部图像进行缓存。
