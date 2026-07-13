---
description: 浏览器中点击操作的目标。
solution: Experience Manager
title: 图像映射
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
TQID: 'https://experienceleague.adobe.com/ikMxCQ23L0HzbfmRlcYGL-fRJFK2uhwbZHNzcy1c25k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

浏览器中点击操作的目标。

始终与图像关联。 您可以从`ImageInfo`获取`ImageMap`目标。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 图像映射句柄。 |
| [!DNL name] | `xsd:string` | 图像映射名称。 |
| [!DNL region] | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>`标记属性。 |
| [!DNL action] | `xsd:string` | 要包含在HTML `<area>`标记中的其他属性，包括`href` URL。 |
| shapeType | `xsd:boolean` | [!DNL RegionShape]值。 |
| [!DNL position] | `xsd:string` | 以HTML `<area>`元素的[!DNL coords]属性的格式表示的位置。 例如： `coords ="0,0,84,128"`。 |
| [!DNL enabled] | `xsd:boolean` | 如果启用了图像映射，则为True。 |
| lastModified | `xsd:dateTime` | 上次修改图像映射的日期和时间。 |

