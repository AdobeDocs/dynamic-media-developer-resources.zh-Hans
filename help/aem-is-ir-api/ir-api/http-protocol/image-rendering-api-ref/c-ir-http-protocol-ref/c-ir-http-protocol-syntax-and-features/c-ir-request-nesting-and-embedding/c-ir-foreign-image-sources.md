---
description: 图像服务支持访问外部HTTP和FTP服务器上的源图像。
seo-description: 图像服务支持访问外部HTTP和FTP服务器上的源图像。
seo-title: 外国图像源
solution: Experience Manager
title: 外国图像源
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 外国图像源{#foreign-image-sources}

图像服务支持访问外部HTTP和FTP服务器上的源图像。

为或命令指定外 `src=` 来URL `mask=` ;只需用大括号分隔整个嵌入的URL:

` …&src={ *[!DNL foreignUrl]*}&…`

允许完全绝对 `attribute::AllowDirectUrls` URL（如果已设置）和相对 `attribute::RootUrl` 的URL。 如果嵌入了绝对URL并且属性为：如 `AllowDirectUrls` 果为0，或者指定了相对URL且 `attribute::RootUrl` 为空。

服务器根据HTTP响应中包含的缓存头对外部图像进行缓存。
