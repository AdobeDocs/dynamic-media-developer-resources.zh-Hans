---
title: 网络
description: 了解如何使用网络带宽优化来根据实际网络带宽调整提供的图像质量。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 96b60fd5f6e3550993cd7640138df4c9bbf6b955
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

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

网络带宽值基于捆绑的CDN的检测到的客户端值。

## 属性



## 默认

`network=off`

## 示例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 另请参阅

[BFC](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)， [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)， [智能成像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)