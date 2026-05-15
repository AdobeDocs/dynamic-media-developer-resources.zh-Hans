---
description: 图像目录提供了许多服务器配置设置，以及字体、ICC配置文件和命令宏。
solution: Experience Manager
title: 图像目录
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# 图像目录{#image-catalogs}

图像目录提供了许多服务器配置设置，以及字体、ICC配置文件和命令宏。

它们将请求中使用的图像和静态内容ID映射到实际文件路径，存储各种图像元数据（如图像映射），并为模板和图像集提供容器。

图像目录仅由[!DNL Platform Server]访问，而不由图像服务器访问。 目录属性文件必须具有.ini后缀，并置于[!DNL Platform Server]的目录文件夹( `PS::CatalogFolder`)中。 至少需要默认图像目录，并且必须用所有属性填充，以使[!DNL Platform Server]正常工作。
