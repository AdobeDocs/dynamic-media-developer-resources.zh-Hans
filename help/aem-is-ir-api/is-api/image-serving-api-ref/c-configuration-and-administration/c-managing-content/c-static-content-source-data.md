---
description: 静态内容源数据文件只能由平台服务器访问。
seo-description: 静态内容源数据文件只能由平台服务器访问。
seo-title: 静态内容源数据
solution: Experience Manager
title: 静态内容源数据
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 静态内容源数据{#static-content-source-data}

静态内容源数据文件只能由平台服务器访问。

静态内容数据文件的路径解析如下：

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

服务器从右到左组合路径段，直到建立绝对文件路径。

所有 ` *[!DNL rootPath]*` 段可以是空的、相对的或绝对路径段。

` *[!DNL catalogPath]*` 是绝对或相对文件路径／名称。 *[!DNL requestPath]* 必须为相对文件路径／名称。

可以 `PS::staticContent.rootPaths` 在中定义多个值 [!DNL PlatformServer.conf]。 这允许在多个文件系统中分发源数据文件。 平台服务器将按指定的顺序尝试替代路径，直到找到数据文件。
