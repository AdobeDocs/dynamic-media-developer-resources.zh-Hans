---
description: 图像服务支持访问外部HTTP和FTP服务器上的源图像。
solution: Experience Manager
title: 外国图像源
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 外国图像源{#foreign-image-sources}

图像服务支持访问外部HTTP和FTP服务器上的源图像。

为`src=`或`mask=`命令指定外部URL;只需用大括号分隔整个嵌入的URL:

` …&src={ *[!DNL foreignUrl]*}&…`

允许使用完全绝对URL（如果设置了`attribute::AllowDirectUrls`）和相对于`attribute::RootUrl`的URL。 如果嵌入了绝对URL和属性，则会发生错误：`AllowDirectUrls`为0，或者如果指定了相对URL且`attribute::RootUrl`为空。

服务器会根据HTTP响应中包含的缓存标头来缓存外来图像。
