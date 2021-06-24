---
description: 图像目录提供了许多服务器配置设置，以及字体、ICC配置文件、命令宏。
solution: Experience Manager
title: 图像目录
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 图像目录{#image-catalogs}

图像目录提供了许多服务器配置设置，以及字体、ICC配置文件、命令宏。

它们将请求中使用的图像和静态内容ID映射到实际文件路径，存储各种图像元数据（如图像映射），并提供模板和图像集容器。

图像目录只能由Platform Server访问，而不能由Image Server访问。 目录属性文件必须具有.ini后缀，并且必须放在Platform Server的目录文件夹(`PS::CatalogFolder`)中。 至少需要默认的图像目录，且必须使用所有属性填充该目录才能正确运行平台服务器。
