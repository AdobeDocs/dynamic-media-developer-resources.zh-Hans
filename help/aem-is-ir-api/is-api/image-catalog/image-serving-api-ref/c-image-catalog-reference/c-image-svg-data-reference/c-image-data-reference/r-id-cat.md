---
description: 目录记录标识符
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
TQID: 'https://experienceleague.adobe.com/M3stRhM1PHUVUFXTKj-KERQVMOGVolpxUuyNUrRzado'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 7%

---

# Id {#id}

[!DNL Platform Server]用于查找图像数据文件中的记录的索引键值。

通常，如果一个SKU具有多个图像，则使用简短且唯一的图像标识符（如SKU编号），并可能包含某种类型的图像后缀。 也可能是更复杂的字符串，看起来更像文件路径，以支持通过图像服务轻松地对网站进行回溯调整。

## 属性 {#id-properties}

文本字符串。 必需. 图像数据表的主索引键。 在表中，每个catalog：：Id值必须是唯一的。

## 默认 {#id-default}

无。

## 另请参阅 {#id-seealso}

[attribute：：RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
