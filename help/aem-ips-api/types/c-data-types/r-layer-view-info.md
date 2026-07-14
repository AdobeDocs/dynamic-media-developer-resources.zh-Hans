---
description: 图层视图属性。
solution: Experience Manager
title: 图层视图信息
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
TQID: 'https://experienceleague.adobe.com/cx-B-BmcEP6vefJY5tsrNMZcwWIKM-pW0CYfP7BjxMM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 46
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

图层视图属性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| url | `xsd:string` | 表示模板的图像服务器URL。 组合`urlModifier`和`urlPostAp- plyModifier`字段。 |
| urlModifier | `xsd:string` | 在请求或`urlPostApplyModifier`命令之前应用的图像服务协议命令。 |
| urlPostApplyModifier | `xsd:string` | 在`urlModifier`之后应用的图像服务协议命令和请求命令。 |

