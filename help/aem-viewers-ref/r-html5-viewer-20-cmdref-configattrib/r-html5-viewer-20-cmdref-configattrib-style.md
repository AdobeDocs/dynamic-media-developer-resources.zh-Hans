---
title: 样式
description: 样式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
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

CSS文件中的所有资源引用都是针对CSS文件位置解析的，而不是针对调用HTML页面的位置解析的。

## 属性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

可选.

## 默认 {#section-79a827f7a3bb4f36b3d72c309155059e}

无。

## 示例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
