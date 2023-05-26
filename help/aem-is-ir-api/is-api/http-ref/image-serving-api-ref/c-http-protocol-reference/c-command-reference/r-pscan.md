---
description: 渐进式JPEG扫描。 渐进式JPEG以这样的方式显示图像，即它最初完整地显示模糊/低质量的照片。 随着扫描的继续，随着图像数据的下载更充分，它变得越来越清晰。 此参数允许您设置显示整个图像所需的扫描次数（3、4或5）。
solution: Experience Manager
title: pscan
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1afd3a60-e0b6-47d1-b7e4-98a3145782a2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# pscan{#pscan}

渐进式JPEG扫描。 渐进式JPEG以这样的方式显示图像，即它最初完整地显示模糊/低质量的照片。 随着扫描的继续，随着图像数据的下载更充分，它变得越来越清晰。 此参数允许您设置显示整个图像所需的扫描次数（3、4或5）。

`pscan=auto|3|4|5`

每次扫描的实际速度取决于用户系统和接收和解压缩数据的计算机的传输速度。

`Auto` 使用由独立JPEG库计算并取决于颜色模型的扫描设置。 的值 `3`， `4`， `5` 对应于将JPEG文件另存为pjpeg(渐进式JPEG)时在Adobe Photoshop中找到的“扫描”设置。

如果 `pscan` 未设置，则默认为 `auto`.

## 属性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

请求属性。 无论当前图层设置如何，均适用。 如果输出格式不是渐进式JPEG，则忽略。

## 默认 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 示例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 另请参阅 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
