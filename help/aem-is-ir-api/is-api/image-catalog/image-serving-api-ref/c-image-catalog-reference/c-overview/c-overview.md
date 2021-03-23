---
description: 图像目录用于向服务器提供有关图像和支持数据(如字体和ICC用户档案)的信息。
seo-description: 图像目录用于向服务器提供有关图像和支持数据(如字体和ICC用户档案)的信息。
seo-title: 概述
solution: Experience Manager
title: 概述
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---


# 概述{#overview}

图像目录用于向服务器提供有关图像和支持数据(如字体和ICC用户档案)的信息。

图像目录用于向服务器提供有关图像和支持数据(如字体和ICC用户档案)的信息。

每个图像目录都包含所需的目录属性文件和一组可选目录数据文件：

* 图像数据文件，它列出图像和模板及其关联的元数据。
* SVG数据文件，它列出SVG文件及其关联的元数据。
* 宏定义文件，它提供请求宏的定义。
* 字体映射文件，用于跟踪文本字体。
* 用户档案映射文件，用于列出ICC颜色用户档案。
* 规则集文件，用于定义HTTP请求预处理规则。

目录数据文件按目录属性文件中的文件引用与图像目录关联。 同一目录数据文件可由多个图像目录共享。

目录属性文件必须具有[!DNL .ini]文件后缀，并且必须位于平台服务器的目录文件夹(`PlatformServer::catalog.rootPath`)中。 目录数据文件可以位于平台服务器可访问的同一文件夹或任何其他文件夹中。

本文档介绍Dynamic Media图像服务系统的图像目录文件格式。 预期受众是经验丰富的程序员和网站开发人员，他们希望将Dynamic Media图像服务用于Web或自定义应用程序。

假定读者通常熟悉Dynamic Media图像服务系统、一般HTTP协议标准和惯例以及基本的图像术语。
