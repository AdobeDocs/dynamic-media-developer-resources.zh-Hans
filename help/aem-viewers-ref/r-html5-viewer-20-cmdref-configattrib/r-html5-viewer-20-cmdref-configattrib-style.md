---
description: 样式
solution: Experience Manager
title: 样式
feature: Dynamic Media Classic，查看器，SDK/API
role: Developer,Business Practitioner
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 7%

---

# 样式{#style}

您可以从URL查询字符串和配置中应用以下命令。 在URL查询字符串中应用的命令始终优先于配置中存在的相同命令。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 相对或绝对CSS位置。 </p> <p>指定自定义CSS文件的位置。 如果<span class="codeph"><span class="varname"> cssPath</span></span>是相对的，则会根据查看器HTML页面位置和<span class="codeph"> contentUrl=</span>参数的值解析该参数。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS文件中的所有资产引用都将根据CSS文件位置（而不是调用HTML页面的位置）进行解析。

## 属性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

可选。

## 默认 {#section-79a827f7a3bb4f36b3d72c309155059e}

无。

## 示例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
