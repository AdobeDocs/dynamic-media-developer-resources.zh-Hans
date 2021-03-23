---
description: 透视变换。 对图层源图像应用透视变换以填充四边形指定的区域。 图层的其他区域保持透明。
seo-description: 透视变换。 对图层源图像应用透视变换以填充四边形指定的区域。 图层的其他区域保持透明。
seo-title: 透视
solution: Experience Manager
title: 透视
uuid: b22d7b49-db08-48df-80bc-5b7237aea475
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 2%

---


# perspect{#perspective}

透视变换。 对图层源图像应用透视变换以填充四边形指定的区域。 图层的其他区域保持透明。

`perspective= *`perspQuadres`*[, *`选项`*]`

`perspectiveN= *`perspQuadNresOptions`*[, *``*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>透视四边形像素坐标（8个边，用逗号分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>透视四边形标准化坐标（8个边，用逗号分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>重新取样选项（请参阅下面）。 </p></td> 
 </tr> 
</table>

*`perspQuad`* 由复合（或图层0）坐标空间中的四个像素坐标值组成，这些值来自复合图像的左上角。

`perspQuadN` 由四个标准化坐标值组成， `0.0,0.0` 其中对应于复合/图层0图像的左上角和 `1.0,1.0` 右下角。

转换输入图像，使输入图像的左上角映射到第一坐标值`perspQuad[N]`、右上角到第二坐标、右下角到第三坐标、左下角到第四坐标。

>[!NOTE]
>
>`pos=` 可用于进一步定位复合图像中的变换层。

透视四边形坐标可位于复合图像之外。

如果四边形不适合透视变换（例如，如果两个或多个顶点重合，如果三个或所有顶点位于同一行上，或者四边形是自相交或凹入的），则行为是未定义的。

## 质量注意事项{#section-7cc9056afa614300a9b8844d39739fc3}

尽管默认实现在质量和性能之间产生合理的折中，但有时可能需要提高源图像的分辨率以提高清晰度或降低分辨率以减少锯齿伪像。

如果源是图像，请使用`scale=`选择其他分辨率（相对于图像的完整分辨率）。 指定的`scale=`值将舍入到下一个更高的PTIF分辨率级别。 在嵌套请求源的情况下，可以调整由嵌套请求产生的图像的大小以达到所需的锐度。 对于文本层，通过选择较大的size=值并增加使用`textAttr=`指定的分辨率来调整输入图像（渲染的文本）的分辨率。

*`resOptions`* 允许选择替代的重新取样算法。支持以下值（区分大小写）：

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
   <td> <p> 最近的邻居。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> 双线性. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 标准超采样（默认）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3<span class="varname"> Tn</span></span> </p> </td> 
   <td> <p> 具有可调抖动的超采样（<span class="varname"> n</span>必须是介于0和200之间的整数值）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-818e57df0a1b4449888543bc6af77751}

图层命令。 应用于当前图层，或应用于`layer=comp`时的图层0。 被效果图层忽略。

`res=` 当透视显示在同一图层中时，始终忽略。`size=` 当为图像图层指定时将忽略。`size=` 和 `res=` 在图层中 `perspective=` 保留供将来使用。

## 默认 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`, for no perspective transform.

## 另请参阅 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ,  [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065),  [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
