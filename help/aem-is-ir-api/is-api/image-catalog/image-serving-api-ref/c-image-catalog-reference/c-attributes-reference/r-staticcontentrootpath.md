---
description: 静态内容数据根路径。 此图像目录的静态内容数据的根文件夹的绝对路径或相对路径区段。
solution: Experience Manager
title: StaticContentRoot路径
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55ca44cd-4330-47e6-94cc-58c078d34bbd
TQID: 'https://experienceleague.adobe.com/u9O8XaMdnb02UPw1uIjhYjzpFvMk-tFfh3UqlcVnNcc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 2%

---

# StaticContentRoot路径{#staticcontentrootpath}

静态内容数据根路径。 此图像目录的静态内容数据的根文件夹的绝对路径或相对路径区段。

有关服务器根路径的其他信息，请参阅[管理Source数据](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)。

## 属性 {#section-f8e3986096294b36948d43aafdc3e795}

文本字符串。 必须为空、有效的相对文件路径段或绝对路径。 不应包含前导和尾随路径元素分隔符。

## 默认 {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

如果未定义，则从`default::StaticContentsRootPath`继承。 如果已定义但为空，则它不会参与源文件根路径。

## 另请参阅 {#section-9af8846d20d242789df67877f84ed8a7}

[PS：：staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5) ，[管理Source数据](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
