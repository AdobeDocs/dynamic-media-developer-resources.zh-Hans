---
description: 图像渲染配置设置存储在 [!DNL Platform Server] 配置文件。
solution: Experience Manager
title: 配置文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# 配置文件{#configuration-files}

图像渲染配置设置存储在 [!DNL Platform Server] 配置文件。

平台服务器配置文件位于[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此文件是JAVA属性文件。 必须注意遵守适当的公约，否则 [!DNL Platform Server] 可能无法启动。 双反斜线(`\\`)或在Windows文件路径中必须使用单个正斜杠(/)，而不是简单的反斜杠(\)，因为反斜杠在此类型的文件中用作转义字符。 文件包含未记录的属性，这些属性供内部服务器使用，不得修改。

请参阅 [配置设置参考](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) 以查看所有“图像渲染”配置设置的列表。
