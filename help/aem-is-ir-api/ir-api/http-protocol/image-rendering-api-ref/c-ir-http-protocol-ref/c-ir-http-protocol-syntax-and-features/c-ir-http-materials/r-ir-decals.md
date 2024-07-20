---
title: 标记
description: 贴花材料包括服装构造，如套衫、T恤印花和刺绣或印刷的标志。 它还包括在内部或外部应用中使用的非可重复扁平物体，例如区域地毯、壁挂艺术品和标志。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# 标记{#decals}

贴花材料包括服装构造，如套衫、T恤印花和刺绣或印刷的标志。 它还包括在内部或外部应用中使用的非可重复扁平物体，例如区域地毯、壁挂艺术品和标志。

如果在MSS贴花中指定了材料，则将其视为贴花。 贴花通常是RGBA图像，由alpha通道定义贴花的形状。

每个平面、流线、草图、平面或壁对象都可以应用一个贴花（除非设置了“无纹理”标志）。 通过将贴花的`anchor=`与晕影对象的贴花原点对齐，将贴花应用于对象。 可以使用`pos=`进一步调整位置。

如果贴花材料定义厚度并且晕影对象定义光矢量，则呈现投影。

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
   <td colname="col2"> <p>图像（通常使用Alpha）；必需。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph">大小= </span> </a> </p> </td> 
   <td colname="col2"> <p>贴花宽度、高度和厚度（用于投影）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph">分辨率</span>，<span class="varname"> imageHeight </span> x <span class="codeph">分辨率，0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph">资源= </span> </a> </p> </td> 
   <td colname="col2"> <p>纹理分辨率（如果指定size= ，则忽略）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">属性：：分辨率</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph">锚点= </span> </a> </p> </td> 
   <td colname="col2"> <p>贴花对齐点。 </p> </td> 
   <td colname="col3"> <p>图像中心。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>相对贴花位置。 </p> </td> 
   <td colname="col3"> <p>0， 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>贴花不透明度。 </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </td> 
   <td colname="col2"> <p>锐化。 </p> </td> 
   <td colname="col3"> <p>0（无锐化） </p> </td> 
  </tr> 
 </tbody> 
</table>
