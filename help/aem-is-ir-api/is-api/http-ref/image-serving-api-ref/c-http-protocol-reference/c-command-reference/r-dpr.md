---
title: dpr
description: 设备像素比率(DPR)&amp；mdash；也称为CSS像素比率&amp；mdash；是设备的物理像素与逻辑像素之间的关系。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d64ca9ed-7d8e-4a13-9c9d-acb7de3e31ed
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 9%

---

# dpr{#dpr}

设备像素比率(DPR)（也称为CSS像素比率）是设备的物理像素与逻辑像素之间的关系。 特别是随着视网膜屏幕的出现，现代移动设备的像素分辨率正以迅速的速度增长。

启用“设备像素比”优化将以屏幕的本机分辨率呈现图像，从而使图像更加清晰。

当前，显示的像素密度来自Akamai CDN标头值。

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">折扣</span> </span> </p> </td> 
  <td class="stentry"> <p>在单个图像URL级别关闭DPR优化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">位于，dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>使用自定义值（任何客户端逻辑或其他方法检测到值）覆盖智能成像检测到的DPR值。 dprValue的允许值是大于0的任意数字。 </p> </td> 
 </tr> 
</table>


即使公司级别的DPR设置为off，您仍可以使用`dpr=on,dprValue`。

由于DPR优化，当生成的图像大于MaxPix Dynamic Media设置时，始终通过保持图像的宽高比来识别MaxPix宽度。

| 请求的图像大小 | DPR值 | 投放的图像大小 |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

DPR值基于捆绑的CDN中检测到的客户端值。 这些值有时不准确。 例如，具有`dpr=2`的iPhone5和dpr=3的iPhone12均显示`dpr=2`。 但是，对于高分辨率设备，发送`dpr=2`比发送`dpr=1`好。 但是，克服这种不准确性的最佳方法是使用客户端DPR为您提供100%准确的值。 它适用于任何设备，无论是Apple还是任何其他已启动的设备。 请参阅[使用客户端设备像素比](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en)的智能成像。

## 属性

请求属性。 如果`dpr`关闭或`dprValue=1`，则它不起作用。

## 默认

`dpr=off`


## 示例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 另请参阅

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)，[网络](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md)，[智能成像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
