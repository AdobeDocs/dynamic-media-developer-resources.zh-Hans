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

您可以從URL查詢字串和設定中套用以下命令。 URL查詢字串中套用的命令一律優先於config中顯示的相同命令。

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> 相對或絕對CSS位置。 </p> <p>指定自訂CSS檔案的位置。 如果 <span class="codeph"><span class="varname"> cssPath</span></span> 是相對的，則會根據檢視器HTML頁面位置與的值來解析 <span class="codeph"> contentUrl=</span> 引數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

CSS檔案內的所有資產參考都是根據CSS檔案位置來解析，而非根據呼叫HTML頁面的位置來解析。

## 屬性 {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

可选.

## 默认 {#section-79a827f7a3bb4f36b3d72c309155059e}

无。

## 示例 {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
