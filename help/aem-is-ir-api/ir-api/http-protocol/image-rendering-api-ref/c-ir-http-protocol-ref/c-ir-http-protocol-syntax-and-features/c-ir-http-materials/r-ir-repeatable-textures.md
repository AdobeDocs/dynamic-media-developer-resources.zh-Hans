---
description: 可重复的纹理包括内部和外部材料，如织物（包括服装和内饰）、墙到墙地板覆盖物、墙纸、台面材料、木纹纹理、屋面和壁板材料，以及任何其他通用纹理。
solution: Experience Manager
title: 可重复的纹理
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---

# 可重复的纹理{#repeatable-textures}

可重复的纹理包括内部和外部材料，如织物（包括服装和内饰）、墙到墙地板覆盖物、墙纸、台面材料、木纹纹理、屋面和壁板材料，以及任何其他通用纹理。

可重复的纹理可应用于平面、流线、草图、平面、壁和机柜对象。 当应用于非可纹理化对象时，该对象将用`color=`（如果未指定`color=`，则使用`bgc=`）进行绘制。

如果材料包含指定图像的`src=`属性，并且该材料出现在除贴图或壁边框以外的MSS中，则该材料被视为纹理。

在渲染时，通过将纹理材料的`anchor=`点与对象的纹理原点匹配（如晕影中创作的），将纹理与对象对齐。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>可重复纹理图像；必需 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>纹理分辨率 </p> </td> 
   <td colname="col3"> <span class="codeph"> 属性：:Resolution  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 锚点=  </span> </a> </p> </td> 
   <td colname="col2"> <p>纹理对齐点 </p> </td> 
   <td colname="col3"> <p>左上角。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>重复模式 </p> </td> 
   <td colname="col3"> <p>0（直重复）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> 格劳特=  </span> </a> </p> </td> 
   <td colname="col2"> <p>灌浆颜色和厚度；用于陶瓷/石材瓷砖材料 </p> </td> 
   <td colname="col3"> <p>图像中已存在的Grout </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align=  </span> </a> </p> </td> 
   <td colname="col2"> <p>对齐模式（对象之间）；用于装饰用品 </p> </td> 
   <td colname="col3"> <p>中心匹配 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>纹理旋转角度；不支持壁对象 </p> </td> 
   <td colname="col3"> <p>0（无旋转） </p> </td> 
  </tr> 
 </tbody> 
</table>
