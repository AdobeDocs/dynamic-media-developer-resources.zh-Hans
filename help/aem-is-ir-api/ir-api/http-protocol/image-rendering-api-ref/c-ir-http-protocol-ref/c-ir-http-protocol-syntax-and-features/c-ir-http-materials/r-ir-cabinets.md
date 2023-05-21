---
title: 檔案櫃
description: 檔案櫃材料指定了檔案櫃樣式檔案（.vnc副檔名），這是一個特殊的資料檔案，其中包含檔案櫃的攝影表示以及引數配置圖定義和呈現檔案櫃正面所需的其他資訊。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 4%

---

# 檔案櫃{#cabinets}

檔案櫃材料指定了檔案櫃樣式檔案（.vnc副檔名），這是一個特殊的資料檔案，其中包含檔案櫃的攝影表示以及引數配置圖定義和呈現檔案櫃正面所需的其他資訊。

[!DNL vnc] 檔案可能包含可重複的木紋紋理，或是紋理可以透過第二個引數從外部提供。 `src=`. 特定 [!DNL vnc] 檔案可讓機櫃正面選取的區域色彩化或紋理化（通常用於層壓機櫃樣式）。

機櫃材料只能套用至機櫃物件。

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
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
   <td colname="col2"> <p>封包樣式檔案；必填。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>選用的紋理影像檔案(第二個值 <span class="codeph"> src= </span>)。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>選用的紋理解析度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute：：Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>為機櫃和/或紋理上色。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>锐化. </p> </td> 
   <td colname="col3"> <p>0 （無銳利化） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> 旗標= </span> </a> </p> </td> 
   <td colname="col2"> <p>特殊轉譯器旗標。 </p> </td> 
   <td colname="col3"> <p>0 （無旗標） </p> </td> 
  </tr> 
 </tbody> 
</table>
