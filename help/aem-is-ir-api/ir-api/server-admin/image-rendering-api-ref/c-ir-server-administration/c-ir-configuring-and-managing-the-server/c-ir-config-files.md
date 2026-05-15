---
description: 图像渲染配置设置存储在 [!DNL Platform Server] 配置文件中。
solution: Experience Manager
title: 配置文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
TQID: 'https://experienceleague.adobe.com/KTBXtuSOstPMi7bPQg70jyUVCqcXlLiLPiFFhyp9iFg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# 配置文件{#configuration-files}

图像渲染配置设置存储在[!DNL Platform Server]配置文件中。

平台服务器配置文件位于[!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]。 此文件是一个JAVA属性文件。 必须注意遵循相应的惯例，否则[!DNL Platform Server]可能无法启动。 在Windows文件路径中，必须使用双反斜杠(`\\`)或单正斜杠(/)，而不是简单的反斜杠(\)，因为反斜杠在此类型的文件中用作转义字符。 该文件包含未记录的属性，这些属性供内部服务器使用，不得修改。

有关所有图像渲染配置设置的列表，请参阅[配置设置引用](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81)。
