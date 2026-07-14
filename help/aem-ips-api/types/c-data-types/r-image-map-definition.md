---
description: 浏览器中点击操作的目标定义。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
TQID: 'https://experienceleague.adobe.com/x27LpaNACQ5k-n09O-9Bhw7aecAjWQ6wNkLt8XewVXs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

浏览器中点击操作的目标定义。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 名称 | `xsd:string` | 图像映射定义的名称。 |
| shapeType | `xsd:string` | 区域形状值之一。 |
| 地区 | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>`标记属性。 |
| 操作 | `xsd:string` | 要包含在HTML `<area>`标记中的其他属性，包括`href` URL。 |
| 已启用 | `xsd:boolean` | 如果启用了图像映射，则为True。 |

