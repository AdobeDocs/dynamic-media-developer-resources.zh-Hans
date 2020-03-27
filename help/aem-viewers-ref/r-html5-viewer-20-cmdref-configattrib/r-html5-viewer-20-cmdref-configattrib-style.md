---
description: 'null'
seo-description: 'null'
seo-title: 样式
solution: Experience Manager
title: 样式
topic: Dynamic media
uuid: 6320c8dd-4827-41dc-a621-6fdf22e55003
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# style{#style}

可以从URL查询字符串和配置中应用以下命令。 在URL查询字符串中应用的命令始终优先于配置中存在的同一命令。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> css路径</span></span> </p> </td> 
   <td colname="col2"> <p> 相对或绝对CSS位置。 </p> <p>指定自定义CSS文件的位置。 如果 <span class="codeph"><span class="varname"> cssPath是相对的</span></span> ，则会根据查看器HTML页面位置和contentUrl=参数的值解析 <span class="codeph"> 它</span> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS文件中的所有资源引用将根据CSS文件位置（而非调用HTML页面的位置）进行解析。

## 属性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

可选。

## 默认 {#section-79a827f7a3bb4f36b3d72c309155059e}

无。

## 示例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
