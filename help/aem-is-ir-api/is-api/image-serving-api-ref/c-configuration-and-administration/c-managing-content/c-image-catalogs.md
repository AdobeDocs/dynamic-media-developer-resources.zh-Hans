---
description: 图像目录提供了许多服务器配置设置，以及字体、ICC配置文件、命令宏。
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

图像目录提供了许多服务器配置设置，以及字体、ICC配置文件、命令宏。

它们将请求中使用的图像和静态内容ID映射到实际文件路径，存储各种图像元数据（如图像映射），并提供模板和图像集容器。

图像目录仅由 [!DNL Platform Server]，从不由图像服务器执行。 目录属性文件必须具有.ini后缀，并且位于 [!DNL Platform Server]&#39;s目录文件夹( `PS::CatalogFolder`)。 至少需要默认的图像目录，且必须填充所有属性才能正确运行 [!DNL Platform Server].
