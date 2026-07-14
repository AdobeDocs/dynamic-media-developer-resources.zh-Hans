---
description: 在服务器处于活动状态时，可以使用req=release命令在覆盖文件之前替换或删除晕影文件。
solution: Experience Manager
title: 删除或替换源数据文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
TQID: 'https://experienceleague.adobe.com/clXDwtsKfD4WkpgNvoJoXG19WvFkcOhdjtTGmoArpv4'
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
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 0%

---

# 删除或替换源数据文件{#deleting-or-replacing-source-data-files}

在服务器处于活动状态时，可以使用req=release命令在覆盖文件之前替换或删除晕影文件。

>[!NOTE]
>
>在渲染服务器访问数据文件时，不得替换或删除数据文件。

请记住，删除或替换源数据文件只会导致渲染服务器关闭该文件，直到访问晕影的下一次请求为止。 如果文件使用量很大，可能需要多次重试。

必须停止渲染服务器才能替换其他数据文件。

替换材质文件或晕影时，[!DNL Platform Server]缓存条目会自动失效。 替换ICC配置文件不会使缓存失效。

为了避免替换文件带来的麻烦，建议为替换文件提供一个新名称并更新相应的目录条目。 这允许在服务器处于活动状态时替换任何数据文件，并导致服务器缓存条目自动失效，而无需其他干预。 此方法可用于由图像目录管理的所有数据文件。

