---
title: DigimarcInfo
description: Digimarc影像資訊。 啟用Digimarc內嵌，並指定浮水印型別和任何相關的影像特定資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 14%

---

# DigimarcInfo{#digimarcinfo}

Digimarc影像資訊。 啟用Digimarc內嵌，並指定浮水印型別和任何相關的影像特定資料。

## 屬性 {#section-62af219e8bac422b8541841221c9ce4f}

四個整數值，以逗號分隔。

`*`type`*, *`標幟`*, *`val1`*, *`val2`*`

`*`type`*` 啟用Digimarc嵌入並指定浮水印型別：

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>浮水印型別</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>基本. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>图像 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>交易 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>版權年份。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`標幟`*` 是包含三個值的位元欄位。 設定位元0表示受複製保護的內容，位元1表示受限制的內容，位元2表示成人內容：

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 標幟</span> </span> </p> </th> 
   <th class="entry"> <p><b>说明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>有複製保護。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>受限制。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>受複製保護、受限制。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>成熟的內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>複製受保護的成人內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>受限的成人內容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>受複製保護、受限制、成熟的內容。 </p> </td> 
  </tr> 
 </tbody> 
</table>

對的解讀 `*`val1`*` 和 `*`val2`*` 依據 `*`type`*`：

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>图像 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>交易 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>第一個版權年。 </p> </td> 
   <td> <p>第二著作權年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 默认 {#section-4bb97e5f79074be89cc691e73449eb43}

如果欄位不存在或為空，則繼承自attribute：：DigimarcInfo。

## 示例 {#section-0f14727a0a2a408781c9df71fed7f42d}

「0,0，0,0」會停用此影像的Digimarc浮水印。

「1,5，0,0」會指定設定了成人及受複製保護內容標幟的基本浮水印。

「2,0，4567,0」會指定包含影像ID的浮水印。

「3,2，56483，0」會指定包含交易ID和已設定受限制內容旗標的浮水印。

「4,0，1998,2001」指定了包含版權年份的浮水印。

## 另请参阅 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute：：DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ， [attribute：：DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
