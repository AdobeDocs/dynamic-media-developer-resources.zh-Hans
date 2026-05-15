---
title: pathEmbed
description: 嵌入路径数据。 指定是否应将来自0层源图像文件的Photoshop路径包含在响应图像中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
TQID: 'https://experienceleague.adobe.com/ES7nAoYjO6Y4naU2c5TIPotPUTjncwjRMLL7-4--XpE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# pathEmbed{#pathembed}

嵌入路径数据。 指定是否应将来自0层源图像文件的Photoshop路径包含在响应图像中。

`pathEmbed=0|1`

## 属性 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

请求属性。 如果源图像不包含路径数据，则忽略。 路径数据像图像数据一样被缩放和旋转。 仅处理来自`layer=0`的源图像的路径；忽略来自其他图层图像的路径。

如果输出图像格式不支持路径嵌入，则忽略。 有关支持路径嵌入的输出图像格式列表，请参阅`fmt=`的说明。

## 限制 {#section-697cddb79a1542bc8457d2f4f59eec69}

目前不支持将开放Photoshop路径（不构成封闭循环的路径）嵌入响应图像。

## 默认 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`，用于在输出图像中不嵌入路径。

## 另请参阅 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
