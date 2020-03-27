---
description: 装饰材料包括服装构造体，如花饰、T恤印花、刺绣或印刷徽标，以及内部或外部应用中使用的不可重复的扁平物品，如地毯、挂壁艺术、标志等。
seo-description: 装饰材料包括服装构造体，如花饰、T恤印花、刺绣或印刷徽标，以及内部或外部应用中使用的不可重复的扁平物品，如地毯、挂壁艺术、标志等。
seo-title: Decals
solution: Experience Manager
title: Decals
topic: Scene7 Image Serving - Image Rendering API
uuid: 6e64f382-f15f-4018-b00c-4fd21a4ebc8c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Decals{#decals}

装饰材料包括服装构造体，如花饰、T恤印花、刺绣或印刷徽标，以及内部或外部应用中使用的不可重复的扁平物品，如地毯、挂壁艺术、标志等。

如果材料在10个MSS中指定，则该材料被视为10个。 贴图通常是RGBA图像，其alpha渠道定义贴图的形状。

可以将一个贴面应用于每个平面、流线、草图、平面或墙对象（除非设置“无纹理”标志）。 通过使贴面与暗角对象的贴面来源点对 `anchor=` 齐，贴面被应用于对象。 该位置可进一步调整 `pos=`。

如果贴心材料限定厚度，而暗角对象限定光矢量，则渲染投影。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>图像（通常使用alpha）;必填。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> 大小= </span></a> </p> </td> 
   <td colname="col2"> <p>倾斜宽度、高度和厚度（用于投影）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, imageHeight <span class="varname"> x </span><span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>纹理分辨率（如果指定size=，则忽略）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 属性：:Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> 锚= </span></a> </p> </td> 
   <td colname="col2"> <p>倾斜对齐点。 </p> </td> 
   <td colname="col3"> <p>图像中心。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> 零点= </span></a> </p> </td> 
   <td colname="col2"> <p>相对倾斜位置。 </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span></a> </p> </td> 
   <td colname="col2"> <p>Decal opacity. </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> 锐= </span></a> </td> 
   <td colname="col2"> <p>锐化. </p> </td> 
   <td colname="col3"> <p>0（无锐化） </p> </td> 
  </tr> 
 </tbody> 
</table>

