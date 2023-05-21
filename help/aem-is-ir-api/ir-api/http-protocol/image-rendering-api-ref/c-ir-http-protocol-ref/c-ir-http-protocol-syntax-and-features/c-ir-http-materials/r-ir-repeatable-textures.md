---
title: 可重複的紋理
description: 可重複材質包括內部和外部材質，例如織物（包括服裝和室內裝飾）、全牆地板、壁紙、檯面材質、木紋材質、屋頂和側邊材質，以及任何其他一般材質。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 3%

---

# 可重複的紋理{#repeatable-textures}

可重複材質包括內部和外部材質，例如織物（包括服裝和室內裝飾）、全牆地板、壁紙、檯面材質、木紋材質、屋頂和側邊材質，以及任何其他一般材質。

可重複紋理可套用至平面、流動線、草繪、平面、壁和機櫃物件。 當套用至不可紋理的物件時，該物件會使用下列專案上色： `color=` (或 `bgc=` 如果 `color=` 未指定)。

如果材質包含 `src=` 屬性指定影像，以及如果影像出現在貼花或牆壁邊框以外的MSS中。

彩現時，紋理會透過比對 `anchor=` 與物件材質原點相同的材質材質材質點（在暈映中撰寫）。

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
   <th colname="col3" class="entry"> <p>默认 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>可重複的紋理影像；必要 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度 </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute：：Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理對齊點 </p> </td> 
   <td colname="col3"> <p>左上角。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>重複模式 </p> </td> 
   <td colname="col3"> <p>0 （直接重複）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>锐化 </p> </td> 
   <td colname="col3"> <p>0 （無銳利化）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

除了這些基本屬性之外，可重複的紋理還支援下列進階應用程式的特殊用途屬性：

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
   <th colname="col3" class="entry"> <p>默认 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> 格勞特= </span> </a> </p> </td> 
   <td colname="col2"> <p>灌漿色彩和厚度；適用於陶瓷/石材瓦片材料 </p> </td> 
   <td colname="col3"> <p>群組已存在於影像中 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>對齊模式（物件之間）；用於裝飾應用程式 </p> </td> 
   <td colname="col3"> <p>居中對齊 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理旋轉角度；壁物件不支援 </p> </td> 
   <td colname="col3"> <p>0 （無旋轉） </p> </td> 
  </tr> 
 </tbody> 
</table>
