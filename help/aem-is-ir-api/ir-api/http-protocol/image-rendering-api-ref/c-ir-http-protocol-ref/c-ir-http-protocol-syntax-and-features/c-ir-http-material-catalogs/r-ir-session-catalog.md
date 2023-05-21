---
title: 工作階段目錄
description: 作業階段目錄是材料目錄，為請求提供作業階段屬性，所有src=、vignette=和icc=指令都提供預設catId值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 工作階段目錄{#session-catalog}

作業階段目錄是材料目錄，它提供請求的作業階段屬性，以及預設的catId值 `src=`， `vignette=`、和 `icc=` 命令。

工作階段目錄會指定為HTTP要求路徑的第一個路徑元素（緊接在伺服器名稱后面）。 如果第一個路徑元素與任何目錄的attribute：：RootId不相符，則會使用預設目錄作為工作階段目錄。

工作階段目錄提供下列工作階段預設值：

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：RootPath</span> </p> </td> 
   <td> <p> 材質資料檔案的根路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：VignettePath</span> </p> </td> 
   <td> <p> 暈映檔案的根路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：IccProfileRgb</span> </p> </td> 
   <td> <p> 如果暈映未內嵌ICC設定檔，則為預設的工作色域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：RootUrl</span> </p> </td> 
   <td> <p> 中的相對HTTP檔案路徑的根URL <span class="codeph"> src=</span> 命令 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重疊物件的初始顯示/隱藏狀態 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：Expiration</span> </p> </td> 
   <td> <p> Proxy伺服器和瀏覽器快取回覆影像的存留時間值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：MaxPix</span> </p> </td> 
   <td> <p> 允許的回覆影像寬度和高度上限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：DefaultPix</span> </p> </td> 
   <td> <p> 的預設值 <span class="codeph"> wid=</span> 和 <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：Format</span> </p> </td> 
   <td> <p> 的預設值 <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：JpegQuality</span> </p> </td> 
   <td> <p> 的預設值 <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：TiffEncoding</span> </p> </td> 
   <td> <p> TIFF影像輸出的壓縮型別 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：Sharpen</span> </p> </td> 
   <td> <p> 的預設值 <span class="codeph"> 銳利化=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：OnFailSel</span> </p> </td> 
   <td> <p> 指定下列情況時的行為： <span class="codeph"> sel=</span> 命令失敗 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute：：OnFailObj</span> </p> </td> 
   <td> <p> 指定下列情況時的行為： <span class="codeph"> obj=</span> 命令失敗 </p> </td> 
  </tr> 
 </tbody> 
</table>
