---
description: 嵌入路径数据。 指定是否应将来自0层源图像文件的Photoshop路径包含在响应图像中。
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# pathEmbed{#pathembed}

嵌入路径数据。 指定是否应将来自0层源图像文件的Photoshop路径包含在响应图像中。

`pathEmbed=0|1`

## 属性 {#section-26eb1c9e13574a0eae39f6d5b92c8995}

请求属性。 如果源图像不包含路径数据，则忽略。 路径数据会像图像数据一样缩放和旋转。 只处理`layer=0`源图像的路径；忽略来自其他图层图像的路径。

如果输出图像格式不支持路径嵌入，则忽略。 有关支持路径嵌入的输出图像格式的列表，请参阅`fmt=`的说明。

## 限制{#section-697cddb79a1542bc8457d2f4f59eec69}

此时，不支持将开放Photoshop路径（不形成闭合循环的路径）嵌入到响应图像中。

## 默认 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, for no embedding of paths in output images.

## 另请参阅 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
