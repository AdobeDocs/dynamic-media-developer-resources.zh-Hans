---
description: 建立暈映的新發佈格式。
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 5%

---

# createVignettePublishFormat{#createvignettepublishformat}

建立暈映的新發佈格式。

暈映格式會指定已發佈暈映及其縮圖的大小，以及縮放等級、銳利化引數和從IPS發佈至「影像演算」伺服器的主要暈映所產生暈映的檔案格式版本。

較新的影像演算伺服器版本可支援金字塔暈映，因此無需定義特定的暈映格式大小以進行發佈。

## 授權的使用者型別 {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-3a368186ec1d4005bca056fc9d9bacc7}

**輸入(createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 處理暈映所屬的公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 可識別暈映發佈格式的名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetwidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>指定所產生暈映檢視的目標寬度（畫素）。 </p> <p>使用零，讓輸出暈映的大小與主要暈映相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 建立為影像演算伺服器上的縮放最佳化的金字塔暈映。 從目標暈映大小欄位設定的大小上限開始，這會在單一暈映輸出檔案中建立多個大小檢視。 每個後續的檢視大小都會減半，直到寬度和高度在128x128畫素以內。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定每個所產生縮圖的寬度（畫素）。 此設定為選用。 保留為0表示沒有縮圖檔案。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定已發佈暈映的檔案格式。 指定影像製作的新版本和影像演算伺服器的舊版本，您必須指定ImageRendering伺服器可讀取的暈映版本。 如果您指定較高的版本，影像演算伺服器將無法讀取已發佈的暈映。 設定為零可發佈最新版本的暈映。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔暈映名稱和表示其寬度的字尾的字元。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔暈映名稱和表示其寬度的字尾的字元。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 銳利化</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 針對每個發佈的暈映大小將銳利化套用至主檢視影像。銳利化可在縮放暈映時補償模糊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 數位銳利化調整遮色片是一種彈性且強大的方式，可增加銳利度，尤其是在掃描的影像中。 這會控制每個超調的幅度（邊緣邊界會變暗和變亮多少）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影響要增強的邊的大小或邊框的寬度，因此較小的半徑會增強較小尺寸的細節。 較高的半徑值可能會在邊緣產生光暈。 精細細節需要較小的半徑，因為相同大小或小於半徑的微小細節會遺失。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 控制要銳利化的最小亮度變化，或濾鏡運作前相鄰色調值必須相距多遠。 此設定可銳利化較銳利的邊緣，同時保留較輕微的邊緣不受接觸。 允許的0到255臨界值範圍。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(createVignettePublishFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | 是 | 已建立暈映格式的控點。 |

## 示例 {#section-0564752d439642b9bb8de2903db6de1e}

此程式碼會建立暈映發佈格式。 建立請求會指定名稱、目標寬度和高度，以及其他必要的值。

**请求**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**响应**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```
