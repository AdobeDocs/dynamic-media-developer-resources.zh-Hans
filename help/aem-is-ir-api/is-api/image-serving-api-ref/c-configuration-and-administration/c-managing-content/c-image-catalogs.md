---
description: 图像目录提供了许多服务器配置设置，以及字体、ICC配置文件和命令宏。
solution: Experience Manager
title: 图像目录
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# 图像目录{#image-catalogs}

图像目录提供了许多服务器配置设置，以及字体、ICC配置文件和命令宏。

它们将请求中使用的图像和静态内容ID映射到实际文件路径，存储各种图像元数据（如图像映射），并为模板和图像集提供容器。

图像目录只能由以下用户访问： [!DNL Platform Server]，而不是图像服务器。 目录属性文件必须具有.ini后缀，并置于 [!DNL Platform Server]的目录文件夹( `PS::CatalogFolder`)。 至少需要默认图像目录，并且必须填充所有属性才能正确运行 [!DNL Platform Server].
