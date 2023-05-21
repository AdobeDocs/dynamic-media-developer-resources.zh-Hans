---
description: 選擇性型別，可讓您選擇特定視訊影格做為縮圖影像。
solution: Experience Manager
title: 縮圖選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 6%

---

# [!DNL ThumbnailOptions]{#thumbnailoptions}

選擇性型別，可讓您選擇特定視訊影格做為縮圖影像。

语法

## 参数 {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：long</span> </td> 
   <td colname="col3"> <p>設定您要用於視訊縮圖的影格時間（從視訊開始起算的毫秒）。 值範圍從0到視訊結尾。 <p>注意：如果您不正確指定時間，系統會將視訊的第一個影格用於縮圖。 另請參閱 <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```
