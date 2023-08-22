---
title: 透视
description: 透视转换。 对图层源图像应用透视变换，以使用四边形填充指定的区域。 图层的其它区域保持透明。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 1%

---

# 透视{#perspective}

透视转换。 对图层源图像应用透视变换，以使用四边形填充指定的区域。 图层的其它区域保持透明。

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>透视四边形像素坐标（8个实数，以逗号分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>透视四边形归一化坐标（8个实数，以逗号分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>重新取样选项（见下文）。 </p></td> 
 </tr> 
</table>

*`perspQuad`* 由复合（或图层0）坐标空间中的四个像素坐标值组成，这些值源自复合图像的左上角。

`perspQuadN` 由四个规范化的坐标值组成，其中 `0.0,0.0` 对应于复合/图层0图像的左上角，并且 `1.0,1.0` 到右下角。

变换输入图像，使得输入图像的左上角映射到第一坐标值 `perspQuad[N]`，右上角到第二个坐标，右下角到第三个坐标，左下角到第四个坐标。

>[!NOTE]
>
>`pos=` 可用于进一步定位复合图像中的变换层。

透视四边形坐标可以位于合成图像之外。

如果四边形不适用于透视变换（例如，如果两个或更多顶点重合，三个或所有顶点位于同一条线上，或者四边形是自相交或凹的），则行为是未定义的。

## 质量注意事项 {#section-7cc9056afa614300a9b8844d39739fc3}

虽然默认实施会在质量和性能之间产生合理的折衷，但有时可能需要提高源图像的分辨率以提高清晰度或降低它以减少锯齿伪像。

如果源是图像，请使用 `scale=` 选择不同的分辨率（相对于图像的完整分辨率）。 指定的 `scale=` 值会四舍五入到下一个更高的PTIF分辨率级别。 在嵌套请求源的情况下，可以调整由嵌套请求生成的图像的大小以获得所需的锐度。 对于文本图层，通过选择较大的size=值并结合增加指定的分辨率来调整输入图像（渲染的文本）的分辨率 `textAttr=`.

*`resOptions`* 允许选择替代的重新取样算法。 支持以下值（区分大小写）：

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> 最近邻居。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> 双线性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 标准超采样（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> 具有可调节的抖动的超采样(<span class="varname"> n</span> 必须是介于0和200之间的整数值)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-818e57df0a1b4449888543bc6af77751}

图层命令。 应用到当前图层，或应用到图层0，如果 `layer=comp`. 被效果层忽略。

`res=` 当透视显示在同一图层中时，将始终被忽略。 `size=` 在为图像图层指定时忽略。 `size=` 和 `res=` 在图层中 `perspective=` 保留供将来使用。

## 默认 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`，表示无透视变换。

## 另请参阅 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[大小=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ， [缩放=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065)， [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)， [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
