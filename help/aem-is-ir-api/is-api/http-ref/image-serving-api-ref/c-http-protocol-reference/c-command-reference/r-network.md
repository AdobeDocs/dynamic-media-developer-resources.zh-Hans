---
title: 网络
description: 了解如何使用网络带宽优化来根据实际网络带宽调整提供的图像质量。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 2%

---

# 网络{#network}

启用“网络带宽”可根据实际网络带宽自动调整所提供的图像质量。 对于较差的网络带宽， [DPR（设备像素比率）](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) 优化会自动关闭，即使它已经打开。

如有需要，贵公司可以通过追加以下内容来选择退出单个映像级别的网络带宽优化 `network=off` 到图像的URL。

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 开|关 </span> </p> </td> 
  <td class="stentry"> <p>指定网络带宽是根据实际网络带宽（打开）调整提供的图像质量，还是关闭网络带宽优化以不调整图像质量。</p> </td> 
 </tr> 
</table>

DPR和网络带宽值基于捆绑的CDN所检测到的客户端值。 这些值有时不准确。 例如，iPhone5与 `dpr=2`和iPhone12和 `dpr=3`，都显示 `dpr=2`. 但是，对于高分辨率设备，发送 `dpr=2` 比发送dpr=1要好。 但是，克服这种不准确性的最佳方法是使用客户端DPR为您提供100%准确的值。 它适用于任何设备，无论是Apple还是任何其他已启动的设备。 请参阅 [使用具有客户端设备像素比的智能成像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## 属性



## 默认

`network=off`

## 示例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 另请参阅

[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)， [智能成像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)