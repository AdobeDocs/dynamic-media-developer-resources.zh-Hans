---
title: 貼花
description: 貼花材料包括服裝結構，例如套衫、T恤印花和刺繡或印刷的標誌。 它也包括內部或外部應用程式中使用的非可重複平坦物件，例如區域地毯、掛牆藝術和標誌。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 3%

---

# 貼花{#decals}

貼花材料包括服裝結構，例如套衫、T恤印花和刺繡或印刷的標誌。 它也包括內部或外部應用程式中使用的非可重複平坦物件，例如區域地毯、掛牆藝術和標誌。

如果在貼花MSS中指定了材料，則將其視為貼花。 貼花通常是RGBA影像，Alpha色版定義貼花的形狀。

一個貼花可套用到每個平面、流程圖、草繪、平面或壁物件（除非已設定「無紋理」旗標）。 貼花會透過對齊貼花的貼花套用到物件 `anchor=` 暈映物件的貼花原點。 位置可透過進一步調整 `pos=`.

如果貼花材料定義厚度，而暈映物件定義光向量，則會演算陰影。

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
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
   <td colname="col2"> <p>影像（通常含Alpha）；必要。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size= </span> </a> </p> </td> 
   <td colname="col2"> <p>貼花寬度、高度和厚度（用於投影）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>， <span class="varname"> imageHeight </span> x <span class="codeph"> res， 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度（如果指定size=，則忽略）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute：：Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span> </a> </p> </td> 
   <td colname="col2"> <p>貼花對齊點。 </p> </td> 
   <td colname="col3"> <p>影像中心。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>相對貼花位置。 </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>貼花不透明度。 </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </td> 
   <td colname="col2"> <p>锐化. </p> </td> 
   <td colname="col3"> <p>0 （無銳利化） </p> </td> 
  </tr> 
 </tbody> 
</table>
