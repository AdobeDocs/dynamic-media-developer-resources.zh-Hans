---
title: 网络
description: 了解如何使用网络带宽优化来根据实际网络带宽调整提供的图像质量。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
TQID: 'https://experienceleague.adobe.com/9odHf3s93xaQyc1WSkXGamAgoQP070p7ItB9HhyT-dQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 3%

---

# 网络{#network}

启用“网络带宽”可根据实际网络带宽自动调整所提供的图像质量。 对于较差的网络带宽，[DPR（设备像素比）](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)优化会自动关闭，即使它已经打开。

如果需要，贵公司可以通过将`network=off`附加到映像的URL来选择退出单个映像级别的网络带宽优化。

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">开启|关闭</span> </p> </td> 
  <td class="stentry"> <p>指定网络带宽是根据实际网络带宽（打开）调整提供的图像质量，还是关闭网络带宽优化以不调整图像质量。</p> </td> 
 </tr> 
</table>

网络带宽值基于捆绑的CDN的检测到的客户端值。

## 属性

请求属性。 如果网络状况良好，则不会产生任何影响。

## 默认

`network=off`

## 示例

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## 另请参阅

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md)，[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md)，[智能成像](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)
