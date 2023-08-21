---
title: dpr
description: 设备像素比率(DPR)&mdash；也称为CSS像素比率&mdash；是设备的物理像素与逻辑像素之间的关系。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---

# dpr{#dpr}

设备像素比率(DPR)（也称为CSS像素比率）是设备的物理像素与逻辑像素之间的关系。 特别是随着视网膜屏幕的出现，现代移动设备的像素分辨率正以迅速的速度增长。

启用“设备像素比”优化将以屏幕的本机分辨率呈现图像，从而使图像更加清晰。

当前，显示的像素密度来自Akamai CDN标头值。

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 关 </span> </span> </p> </td> 
  <td class="stentry"> <p>在单个图像URL级别关闭DPR优化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 开启，dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>使用自定义值（任何客户端逻辑或其他方法检测到值）覆盖智能成像检测到的DPR值。 dprValue的允许值是大于0的任意数字。 </p> </td> 
 </tr> 
</table>


您可以使用 `dpr=on,dprValue` 即使公司级别的DPR设置为“关闭”。

由于DPR优化，当生成的图像大于MaxPix Dynamic Media设置时，始终通过保持图像的宽高比来识别MaxPix宽度。

| 请求的图像大小 | DPR值 | 投放的图像大小 |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

## 属性



## 默认

`dpr=off`


## 示例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## 另请参阅

[网络](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md)， [智能成像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)