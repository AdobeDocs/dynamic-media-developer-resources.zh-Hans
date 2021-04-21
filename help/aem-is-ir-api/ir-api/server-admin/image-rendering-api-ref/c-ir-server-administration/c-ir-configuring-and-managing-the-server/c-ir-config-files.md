---
description: 图像渲染配置设置存储在平台服务器配置文件中。
solution: Experience Manager
title: 配置文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# 配置文件{#configuration-files}

图像渲染配置设置存储在平台服务器配置文件中。

平台服务器配置文件位于[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此文件是JAVA属性文件。 必须注意遵守相应的约定，否则平台服务器可能无法开始。 在Windows文件路径中，必须使用多次反斜杠(`\\`)或单个正斜杠(/)代替简单反斜杠(\)，因为反斜杠在此类文件中用作转义字符。 文件包含未声明的属性，这些属性供内部服务器使用，不得修改。

有关所有图像渲染配置设置的列表，请参阅[配置设置参考](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)。
