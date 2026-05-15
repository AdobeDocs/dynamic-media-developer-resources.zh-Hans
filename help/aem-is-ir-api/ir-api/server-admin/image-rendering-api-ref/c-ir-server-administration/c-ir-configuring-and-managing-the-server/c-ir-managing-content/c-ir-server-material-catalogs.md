---
description: 材质目录提供了许多图像渲染配置设置。
solution: Experience Manager
title: 材料目录
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
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
source-wordcount: 108
ht-degree: 0%

---

# 材料目录{#material-catalogs}

材质目录提供了许多图像渲染配置设置。

材料目录将请求中使用的晕影和材料ID映射到实际文件路径，可以存储与材料关联的所有元数据，并为模板提供容器。 它们跟踪ICC配置文件和命令宏。

材质目录仅由图像渲染的Java组件访问（与[!DNL Platform Server]共存）。 目录属性文件必须具有[!DNL .ini]后缀，并放置在已注册的目录文件夹中([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7))。 默认材质目录([!DNL default.ini])必须始终存在，并且必须使用所有属性填充才能正确运行图像服务。
