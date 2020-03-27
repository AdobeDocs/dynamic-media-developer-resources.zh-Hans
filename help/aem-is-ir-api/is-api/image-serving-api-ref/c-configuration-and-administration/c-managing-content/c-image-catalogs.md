---
description: 图像目录提供许多服务器配置设置，以及字体、ICC用户档案、命令宏。
seo-description: 图像目录提供许多服务器配置设置，以及字体、ICC用户档案、命令宏。
seo-title: 图像目录
solution: Experience Manager
title: 图像目录
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像目录{#image-catalogs}

图像目录提供许多服务器配置设置，以及字体、ICC用户档案、命令宏。

它们将请求中使用的图像和静态内容ID映射到实际文件路径，存储各种图像元数据（如图像映射），并为模板和图像集提供容器。

图像目录只能由平台服务器访问，而不能由图像服务器访问。 目录属性文件必须具有。ini后缀并放在平台服务器的目录文件夹( `PS::CatalogFolder`)中。 至少需要默认图像目录，并且必须填充所有属性才能使平台服务器正常工作。
