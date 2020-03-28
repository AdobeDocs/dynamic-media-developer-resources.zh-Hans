---
description: 可重复的纹理包括内部和外部材料，如织物（服装和室内装饰）、墙对壁地板覆盖物、墙纸、台面材料、木纹纹理、屋面和壁板材料，以及任何其他通用纹理。
seo-description: 可重复的纹理包括内部和外部材料，如织物（服装和室内装饰）、墙对壁地板覆盖物、墙纸、台面材料、木纹纹理、屋面和壁板材料，以及任何其他通用纹理。
seo-title: 可重复的纹理
solution: Experience Manager
title: 可重复的纹理
topic: Scene7 Image Serving - Image Rendering API
uuid: 11a55d9f-a1d7-490e-af0e-9bf2c3a35501
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 可重复的纹理{#repeatable-textures}

可重复的纹理包括内部和外部材料，如织物（服装和室内装饰）、墙对壁地板覆盖物、墙纸、台面材料、木纹纹理、屋面和壁板材料，以及任何其他通用纹理。

可重复的纹理可应用于平面、流线、草图、平面、墙和机柜对象。 当应用到非纹理化对象时，将使用(或者，如 `color=` 果未指 `bgc=` 定) `color=` 绘制该对象。

如果材料包括指定图像的属性，并且该材 `src=` 料出现在除贴面或壁边框之外的MSS中，则该材料被视为纹理。

在渲染时，通过将纹理材料的点与对象的纹理来源点匹配（如在暗角中创作的），纹理与对象对齐。 `anchor=`

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>可重复的纹理图像；必需 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>纹理分辨率 </p> </td> 
   <td colname="col3"> <span class="codeph"> 属性：:Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 锚= </span></a> </p> </td> 
   <td colname="col2"> <p>纹理对齐点 </p> </td> 
   <td colname="col3"> <p>左上角。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 重复= </span></a> </p> </td> 
   <td colname="col2"> <p>重复模式 </p> </td> 
   <td colname="col3"> <p>0（直接重复）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 锐= </span></a> </p> </td> 
   <td colname="col2"> <p>锐化 </p> </td> 
   <td colname="col3"> <p>0（无锐化）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

除了这些基本属性之外，可重复的纹理还支持高级应用程序的以下特殊用途属性：

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> 格洛= </span></a> </p> </td> 
   <td colname="col2"> <p>灌浆颜色和厚度；用于陶瓷／石砖材料 </p> </td> 
   <td colname="col3"> <p>图像中已存在的Grout </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> 对齐= </span></a> </p> </td> 
   <td colname="col2"> <p>对齐模式（对象之间）;用于室内装饰 </p> </td> 
   <td colname="col3"> <p>中心匹配 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>纹理旋转角度；不支持墙对象 </p> </td> 
   <td colname="col3"> <p>0（无旋转） </p> </td> 
  </tr> 
 </tbody> 
</table>

