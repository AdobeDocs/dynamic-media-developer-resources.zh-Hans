---
description: 本節將說明影像目錄的功能和語法。
solution: Experience Manager
title: 影像目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c83ad2-a932-4df2-92ff-ab34d4a5b1a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# 影像目錄{#image-catalogs}

本節將說明影像目錄的功能和語法。

影像目錄提供下列功能：

* 允許影像與某些中繼資料和修飾元命令持續關聯。

   使用捷徑標籤法參考影像目錄中的專案 `*`rootId/objId`*`，其中 `*`rootId`*` 會識別影像目錄和 `*`物件ID`*` 會識別目錄中的資料記錄。
* 為特定請求屬性提供預設值，例如JPEG品質或是否要套用浮水印。
* 管理字型、ICC設定檔、巨集定義和請求範本

即使未定義特定的影像目錄，影像目錄的所有功能都可透過預設目錄使用( [!DNL default.ini])。

若 `*`rootId`*` 在請求的URL路徑中比對 `attribute::RootId` 特定影像目錄時，該目錄會成為此請求的主要目錄。 主目錄提供整個請求的預設屬性和設定。 如果找不到相符專案，則改用預設目錄。

在中識別的目錄 `src=` 或 `mask=` command為目前圖層提供下列目錄屬性和資料：

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 屬性/資料</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：DefaultExt</span> </p> </td> 
   <td> <p> 目前圖層中所有影像檔案路徑的預設副檔名 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：Expiration</span> </p> </td> 
   <td> <p> 預設 <span class="codeph"> catalog：：到期</span> 如果沒有目錄記錄，則為目前圖層的到期日 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：Icc*</span> </p> </td> 
   <td> <p> 請求和/或目前圖層的工作ICC色彩設定檔、演算色彩比對方式和黑色點補償旗標 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：RootPath</span> </p> </td> 
   <td> <p> 用於目前圖層的所有來源檔案路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：Resolution</span> </p> </td> 
   <td> <p> 預設 <span class="codeph"> catalog：：Resolution</span> 僅限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：錨點</span> </p> </td> 
   <td> <p> 的預設值 <span class="codeph"> anchor=</span> 目前圖層的值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：到期</span> </p> </td> 
   <td> <p> 所有圖層的最小到期值會用作回覆影像的存留時間值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：IccProfile</span> </p> </td> 
   <td> <p> 目前圖層的來源影像色彩設定檔 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：Map</span> </p> </td> 
   <td> <p> 目前圖層的影像地圖資料 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：MaskPath</span> </p> </td> 
   <td> <p> 預設 <span class="codeph"> 遮色片=</span> 目前圖層的 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：Modifier</span> </p> </td> 
   <td> <p> 目前圖層的字首指令(每個指令 <span class="codeph"> catalog：：Modifier</span> 可由URL中的相同命令覆寫（如果針對相同圖層指定） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：Path</span> </p> </td> 
   <td> <p> 目前圖層的來源影像檔案 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：PostModifier</span> </p> </td> 
   <td> <p> 目前圖層的後置處理指令(類似於 <span class="codeph"> catalog：：Modifier</span>，但中的命令 <span class="codeph"> catalog：：PostModifier</span> 覆寫URL中指定的相同命令或 <span class="codeph"> catalog：：Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog：：Resolution</span> </p> </td> 
   <td> <p> 目前圖層的物件解析度 </p> </td> 
  </tr> 
 </tbody> 
</table>

在同一圖層中， `src=` 和 `mask=` 必須參考相同的影像目錄（如果有的話）。

在中識別的目錄 `icc=` 命令僅用於從目錄的ICC設定檔表格中查閱專案。 不涉及其他目錄屬性或資料。

如果， `*`rootId`*` 解析至目錄，並且 `*`物件ID`*` 符合 `catalog::Id` 在此目錄中，然後 `*`rootId/objId`*` 實際上由目錄專案取代，如下所示：

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## 另请参阅 {#section-00e4f6b39cd14244bcce537a3f831259}

[影像目錄參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)， [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)， [遮色片=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)， [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
