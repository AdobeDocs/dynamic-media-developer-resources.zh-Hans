---
title: src
description: 材料檔案。 以單一材質目錄參照的形式，或以一或兩個影像或材質資料檔案（以逗號分隔）指定材質資料。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aff45f0f-e672-40da-9cc8-db83cf3922ff
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 1%

---

# src{#src}

材料檔案。 以單一材質目錄參照的形式，或以一或兩個影像或材質資料檔案（以逗號分隔）指定材質資料。

`src = *`catalogEntry`*|{{ *`材質檔案`*| *`embeddedReq`*}[, *`材質檔案`*]`

`srcE= *`名称`*`

`srcN= *`指数`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> 材質檔案</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 樣式檔案</span>|<span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">大括弧；'是&amp;lbrace；'<span class="varname"> isReq</span>'&amp;rbrace；'&amp;rbrace；|&amp;lbrace；'ir&amp;lbrace；'<span class="varname"> irReq</span>'&amp;rbrace；'|&amp;lbrace；'&amp;lbrace；'<span class="varname"> foreignReq</span>'&amp;rbrace；'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>材質目錄ID (<span class="codeph"> attribute：：RootId</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>材質目錄專案(<span class="codeph"> catalog：：Id</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 樣式檔案</span> </p></td> 
  <td class="stentry"> <p>材料樣式檔案(<span class="filepath"> .vnc</span> 或 <span class="filepath"> .vnw</span>)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>影像資料檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>請求影像伺服。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>請求影像演算。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>向外部伺服器提出要求。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 名称</span> </p></td> 
  <td class="stentry"> <p>內嵌材料的名稱。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 指数</span> </p></td> 
  <td class="stentry"> <p>內嵌材質的0型索引編號。 </p></td> 
 </tr> 
</table>

可重複的紋理、貼花和壁紙材質需要單一影像，可指定為檔案或內嵌要求。

封包材料需要封包樣式的檔案( [!DNL .vnc])，無法指定為巢狀要求。 對於檔案櫃而言，紋理影像檔案是選用的，如果指定，它可以是檔案或內嵌請求。

視窗覆蓋物材料需要視窗覆蓋物樣式檔案( [!DNL .vnw])，無法指定為巢狀要求。 材質檔案是選用的，如果指定，它可以是檔案或內嵌要求。

「影像演算」會使用與「影像伺服」相同的規則來查詢材質目錄、目錄專案及資料檔案。 請參閱 *`object`* 影像伺服檔案中的資料型別，以取得詳細資訊。

*`materialFile`* 是相對於 `attribute::RootPath`.

*`foreignReq`* 可以是相對URL `attribute::RootUrl`，或是絕對URL，如果 `attribute::AllowDirectUrls` 已設定。

若 *`catId`* 未指定，則會使用工作階段目錄。

`srcE=` 和 `srcN=` 提供對暈映中內嵌材料的存取。

## 支援的檔案格式 {#section-f2186d3eef834fc8bbecb2bc68daacad}

影像演算支援與Dynamic Media Image Serving相同的來源影像格式。

需要多個不同解析度影像資料的應用程式，在使用Scene7金字塔TIFF(PTIFF)多解析度格式時表現最佳。 「影像伺服」包含影像轉換器(IC)公用程式，可從任何支援的格式建立PTIFF影像。

如需支援檔案格式的完整清單，請參閱「影像伺服」檔案中的IC公用程式說明。

## 屬性 {#section-e68d03788d534e2184147987d51dfd0f}

材質屬性。 除了純色以外的所有材料都需要（純色材料不允許使用）。 所有字串都區分大小寫。 *`index`* 必須大於或等於0。

## 默认 {#section-dde549c1917540dc8f9555962202da3c}

无。

## 示例 {#section-675865444f8a4d35b9fc6e58b36e3438}

MSS適用於具有獨立可重複紋理的彩色機櫃：

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

材質目錄中可以有相同的材質 `'cat`&#39;在記錄中&#39; `12-3-2`&#39;：

`…&obj=cabinets&src=cat/12-3-2&…`

對「影像伺服」的巢狀要求，以取得紋理影像：

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## 另请参阅 {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[原物料目錄](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2)， [attribute：：RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)， [attribute：：AllowDirectUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
