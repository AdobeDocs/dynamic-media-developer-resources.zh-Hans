---
description: 图像目录用于向服务器提供有关图像和支持数据（如字体和ICC配置文件）的信息。
solution: Experience Manager
title: 概述
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# 概述{#overview}

图像目录用于向服务器提供有关图像和支持数据（如字体和ICC配置文件）的信息。

图像目录用于向服务器提供有关图像和支持数据（如字体和ICC配置文件）的信息。

每个图像目录都由所需的目录属性文件和一组可选的目录数据文件组成：

* 图像数据文件，其中逐项列出了图像和模板及其关联的元数据。
* SVG数据文件，其中详细列出了SVG文件及其关联的元数据。
* 宏定义文件，它提供请求宏的定义。
* 用于跟踪文本字体的字体映射文件。
* 配置文件映射文件，其中列出了ICC颜色配置文件。
* 规则集文件，用于定义HTTP请求预处理规则。

目录数据文件通过目录属性文件中的文件引用与图像目录相关联。 同一目录数据文件可以由多个图像目录共享。

目录属性文件必须具有[!DNL .ini]文件后缀，并且必须位于[!DNL Platform Server]的目录文件夹( `PlatformServer::catalog.rootPath`)中。 目录数据文件可以位于同一文件夹或[!DNL Platform Server]可访问的任何其他文件夹中。

本文档介绍了Dynamic Media图像服务系统的图像目录文件格式。 目标受众是经验丰富的程序员和网站开发人员，他们希望将Dynamic Media图像服务用于Web或自定义应用程序。

假定读者通常熟悉Dynamic Media图像服务系统、一般HTTP协议标准和惯例以及基本的图像术语。
