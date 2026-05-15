---
title: 样式
description: 样式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
TQID: 'https://experienceleague.adobe.com/vkV2CfEEhJmPdQg64y0G-5Ep-T6SPd4tQX88CWbPryw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 7%

---

# 样式{#style}

您可以从URL查询字符串和配置中应用以下命令。 在URL查询字符串中应用的命令始终优先于config中存在的相同命令。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> CSS的相对或绝对位置。 </p> <p>指定自定义CSS文件的位置。 如果<span class="codeph"><span class="varname"> cssPath</span></span>是相对的，则它是针对查看器HTML页面位置和<span class="codeph"> contentUrl=</span>参数的值解析的。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS文件中的所有资源引用都是根据CSS文件位置而不是调用HTML页面的位置解析的。

## 属性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

可选.

## 默认 {#section-79a827f7a3bb4f36b3d72c309155059e}

无。

## 示例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
