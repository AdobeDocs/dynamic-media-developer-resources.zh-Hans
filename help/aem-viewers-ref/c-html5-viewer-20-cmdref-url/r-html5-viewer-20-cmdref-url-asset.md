---
title: asset
description: 所有檢視器通用的引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 2%

---

# asset{#asset}

所有檢視器通用的引數。

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId </span> </span> </p> </td> 
   <td colname="col2"> <p> 單一視訊或自我調整視訊集的資產ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此屬性為必填，除非 `video` 引數。 另請參閱 [外部視訊支援](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) 在視訊底下或 [外部視訊支援](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) 在Video360底下。

或者

` asset= *`图像`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 影像 </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定單一影像或轉盤集。 將雙重HTTP編碼套用至影像名稱或轉盤集名稱中存在的任何不安全字元。 </p> </td> 
  </tr> 
 </tbody> 
</table>

或者

` asset= *`影像`* | *`imageList`* | *`imageListWithModifiers`* | *`multiDimensionSpinSet`* [%3F *`修飾元`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 影像 </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定單一影像。 將雙重HTTP編碼套用至影像名稱中存在的任何不安全字元。 </p> <p>或者，指定影像集的參照。 檢視器會使用從伺服器擷取影像集 <span class="codeph"> req=set IS </span> 要求。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定明確的影像集，由以逗號分隔的專案或影格排序順序組成。 </p> <p> <p>注意：Adobe Dynamic Media Classic支援此功能，Adobe Experience Manager Assets不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定每個影格各有專屬的「影像伺服」修飾元的明確影像集。 在此情況下，框架清單會以括弧括住。 請務必套用兩次HTTP編碼至影格特定「影像伺服」修飾詞中出現的任何逗號。 </p> <p> <p>注意：Adobe Dynamic Media Classic支援此功能，Adobe Experience Manager Assets不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionSpinSet </span> </span> </p> </td> 
   <td colname="col2"> <p>使用以下語法指定明確的多維度迴轉集： </p> <p> <span class="codeph"> (( <span class="varname"> horizontalSpinSet </span>)[，( <span class="varname"> horizontalSpinSet </span>)]) </span> </p> <p> 位置 <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> 是以逗號分隔的指定水平軸框架清單。 全部 <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> 影格數應該相同。 </p> <p> <p>注意：Adobe Dynamic Media Classic支援此功能，Adobe Experience Manager Assets不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 修飾元 </span> </span> </p> </td> 
   <td colname="col2"> <p> 影像伺服命令； <span class="codeph"> 和 </span> 和 <span class="codeph"> = </span> 分隔符號必須使用HTTP編碼為 <span class="codeph"> %26 </span> 和 <span class="codeph"> %3D </span>（分別）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

或者

` asset=( *`mediaSet`* | ( *`視訊`*; *`色票ID`* | *`影像`*; *`色票ID`* | *`setId`*; *`色票ID`*); *`ID`*;( *`視訊`*; *`色票ID`* | *`影像`*; *`色票ID`* | *`setId`*; *`色票ID`*); *`ID`*;] [%3F *`修飾元`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet </span> </span> </p> </td> 
   <td colname="col2"> <p> 指定媒體集的參考。 檢視器會使用req=set IS要求，從伺服器擷取媒體集。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 視訊 </span> </span> </p> </td> 
   <td colname="col2"> <p> 單一視訊或自我調整視訊集。 </p> <p> <p>注意：Adobe Dynamic Media Classic支援此功能，Adobe Experience Manager Assets不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 影像 </span> </span> </p> </td> 
   <td colname="col2"> <p> 單一影像。 </p> <p> <p>注意：Adobe Dynamic Media Classic支援此功能，Adobe Experience Manager Assets不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span> </span> </p> </td> 
   <td colname="col2"> <p> 色票集。 </p> <p> <p>注意：Adobe Dynamic Media Classic支援此功能，Adobe Experience Manager Assets不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 色票ID </span> </span> </p> </td> 
   <td colname="col2"> <p>色票影像。 </p> <p> <p>注意：Adobe Dynamic Media Classic支援此功能，Adobe Experience Manager Assets不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span> </span> </p> </td> 
   <td colname="col2"> <p> 媒體集專案型別識別碼可以是下列其中一項： </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>針對單一影像。 </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>適用於巢狀色票集。 </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> 迴轉 </span> </p> <p>適用於迴轉集。 </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> 視訊 </span> </p> <p>適用於單一視訊。 </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>適用於最適化視訊集。 </p> </li> 
     </ul> </p> <p> <p>注意：Adobe Dynamic Media Classic支援此功能，Adobe Experience Manager Assets不支援。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 修飾元 </span> </span> </p> </td> 
   <td colname="col2"> <p> 影像伺服命令； <span class="codeph"> 和 </span> 和 <span class="codeph"> = </span> 分隔符號必須使用HTTP編碼為 <span class="codeph"> %26 </span> 和 <span class="codeph"> %3D </span>（分別）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此檢視器不支援使用IR （影像演算）或UGC （使用者產生的內容）的影像。

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

必需.

## 默认 {#section-d411e450028c460392cb8508f8ccc5d9}

无。

## 示例 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

單一資產參考：

```
asset=Scene7SharedAssets/Backpack_B
```

或者

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

或者

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

或者

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

或者

```
asset=Viewers/space_station_360-AVS
```

目錄中所定義影像集的單一參照：

```
asset=Viewers/Pluralist
```

明確影像集：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

使用影格特有的「影像伺服」修飾元設定明確的影像：

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

對目錄中定義的迴轉集的單一參照：

```
asset=Scene7SharedAssets/SpinSet-Sample
```

明確迴轉集：

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

明確的多維度迴轉集：

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

單一混合媒體集參考：

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

明確混合媒體集：

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

銳利化修飾元已新增至集中的所有影像：

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```
