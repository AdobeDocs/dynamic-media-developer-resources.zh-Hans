---
description: 样式
solution: Experience Manager
title: 样式
topic: Dynamic Media
uuid: 6320c8dd-4827-41dc-a621-6fdf22e55003
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 8%

---


# style{#style}

您可以从URL查询字符串和配置中应用以下命令。 在URL查询字符串中应用的命令始终优先于配置中存在的同一命令。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 相对或绝对CSS位置。 </p> <p>指定自定义CSS文件的位置。 如果<span class="codeph"><span class="varname"> cssPath</span></span>是相对的，则会根据查看器HTML页面位置和<span class="codeph"> contentUrl=</span>参数的值解析它。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS文件中的所有资源引用都会根据CSS文件位置解析，而不是根据调用HTML页面的位置解析。

## 属性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

可选。

## 默认 {#section-79a827f7a3bb4f36b3d72c309155059e}

无。

## 示例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
