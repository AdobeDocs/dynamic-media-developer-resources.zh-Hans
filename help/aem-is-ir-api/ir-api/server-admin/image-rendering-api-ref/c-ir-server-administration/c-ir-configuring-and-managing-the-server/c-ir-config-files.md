---
description: 图像渲染配置设置存储在平台服务器配置文件中。
solution: Experience Manager
title: 配置文件
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 配置文件{#configuration-files}

图像渲染配置设置存储在平台服务器配置文件中。

平台服务器配置文件位于[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此文件是JAVA属性文件。 必须谨慎遵循相应的惯例，否则Platform Server可能无法启动。 在Windows文件路径中，必须使用双反斜杠(`\\`)或单正斜杠(/)，而不是简单的反斜杠(\)，因为反斜杠在此类文件中用作转义字符。 文件包含未记录的属性，这些属性供内部服务器使用，不得修改。

有关所有图像渲染配置设置的列表，请参阅[配置设置引用](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) 。
