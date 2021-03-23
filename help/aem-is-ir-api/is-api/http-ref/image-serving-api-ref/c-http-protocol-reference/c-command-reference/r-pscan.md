---
description: 渐进式JPEG扫描。 渐进式JPEG以最初显示模糊/低质量照片的方式显示图像。 随着扫描过程的继续，随着图像数据的下载更加完整，扫描过程变得更加清晰。 通过此参数，可以设置显示整个图像所需的扫描次数（3、4或5）。
seo-description: 渐进式JPEG扫描。 渐进式JPEG以最初显示模糊/低质量照片的方式显示图像。 随着扫描过程的继续，随着图像数据的下载更加完整，扫描过程变得更加清晰。 通过此参数，可以设置显示整个图像所需的扫描次数（3、4或5）。
seo-title: pscan
solution: Experience Manager
title: pscan
uuid: c8e1d7a9-679c-437f-aa53-67aca3f40b30
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# pscan{#pscan}

渐进式JPEG扫描。 渐进式JPEG以最初显示模糊/低质量照片的方式显示图像。 随着扫描过程的继续，随着图像数据的下载更加完整，扫描过程变得更加清晰。 通过此参数，可以设置显示整个图像所需的扫描次数（3、4或5）。

`pscan=auto|3|4|5`

每个扫描的实际速度取决于用户系统和接收和解压缩数据的计算机的传输速度。

`Auto` 使用由独立JPEG库计算并取决于颜色模型的扫描设置。`3`、`4`、`5`的值与将JPEG文件另存为pjpeg（渐进式JPEG）时在Adobe Photoshop中找到的“扫描”设置相对应。

如果未设置`pscan`，则默认为`auto`。

## 属性 {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

请求属性。 无论当前图层设置如何，均适用。 如果输出格式不是渐进式JPEG，则忽略。

## 默认 {#section-01948f6cd7a2415091004cd7526436c7}

`pscan=auto`

## 示例 {#section-d51bc4d0e8a9473786f149cba9540506}

`http://localhost:8080/is/image/demo/bedroom.tif?wid=300&fmt=pjpeg&pscan=4`

## 另请参阅 {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
