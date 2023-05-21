---
title: 視窗覆蓋
description: 窗飾材料包括柔軟的窗飾（窗簾、陽台、咖啡館窗簾）和硬的窗飾（色調和百葉窗）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 4%

---

# 視窗覆蓋{#window-coverings}

窗飾材料包括柔軟的窗飾（窗簾、陽台、咖啡館窗簾）和硬的窗飾（色調和百葉窗）。

視窗涵蓋材料指定 *視窗涵蓋樣式檔案* ( [!DNL .vnw] 副檔名)，與暈映類似的特殊資料檔案，包含定義視窗涵蓋範圍的遮色片、照明、版面配置及紋理資料。

[!DNL vnw] 檔案不包含視窗覆蓋的顏色和紋理（織物）。 此資訊會個別指定，類似於可重複的紋理。

視窗覆蓋物件只能套用至重疊物件的視窗覆蓋框架物件。

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
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
   <td colname="col2"> <p>視窗涵蓋樣式檔案；必填。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理影像檔案(的第二個值 <span class="codeph"> src= </span>)。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>紋理解析度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute：：Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>重複模式。 </p> </td> 
   <td colname="col3"> <p>0 （直接重複） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>純色（或為紋理著色）。 </p> </td> 
   <td colname="col3"> <p>128 （中性灰色） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>锐化. </p> </td> 
   <td colname="col3"> <p>0 （無銳利化） </p> </td> 
  </tr> 
 </tbody> 
</table>
