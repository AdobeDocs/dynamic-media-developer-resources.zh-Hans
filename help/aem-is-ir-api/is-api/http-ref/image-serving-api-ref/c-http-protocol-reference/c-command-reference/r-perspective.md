---
title: 透视
description: 透视转换。 对图层源图像应用透视变换，以便使用四边形填充指定的区域。 图层的其它区域保持透明。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# 透视{#perspective}

透视转换。 对图层源图像应用透视变换，以便使用四边形填充指定的区域。 图层的其它区域保持透明。

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

修饰符&#x200B;*`perspQuad`*&#x200B;由复合（或图层0）坐标空间中的四个像素坐标值组成，这些值源自复合图像的左上角。

修饰符`perspQuadN`包含四个规范化的坐标值，其中`0.0,0.0`对应于复合/图层0图像的左上角，`1.0,1.0`对应于右下角。

转换输入图像，使输入图像的左上角映射到`perspQuad[N]`的第一坐标值，右上角映射到第二坐标，右下角映射到第三坐标，左下角映射到第四坐标。

>[!NOTE]
>
>修饰符`pos=`可用于进一步定位复合图像中的转换图层。

透视四边形坐标可以位于合成图像之外。

如果四边形不适用于透视转换，则行为是未定义的。 例如，如果两个或更多顶点重合，如果三个或所有顶点位于同一条线上，或者如果四边形是自相交或凹的。

## 质量注意事项 {#section-7cc9056afa614300a9b8844d39739fc3}

虽然默认实施在质量和性能之间产生了合理的折衷，但可能需要提高源图像的分辨率以提高清晰度或降低它以减少锯齿伪像。

如果源是图像，请使用`scale=`选择不同的分辨率（相对于图像的完整分辨率）。 指定的`scale=`值将舍入到下一个更高的PTIF分辨率级别。 如果存在嵌套请求源，则可以调整由嵌套请求生成的图像的大小以实现所需的锐化。 对于文本图层，通过选择较大的size=值，并增加以`textAttr=`指定的分辨率，来调整输入图像（渲染的文本）的分辨率。

修饰符&#x200B;*`resOptions`*&#x200B;允许您选择替代的重新取样算法。 支持以下值（区分大小写）：

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>值</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
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
   <td> <p> 具有可调整抖动的超采样（<span class="varname"> n</span>必须是从0到200的整数值）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-818e57df0a1b4449888543bc6af77751}

图层命令。 应用于当前图层，或应用于图层0（如果为`layer=comp`）。 被效果层忽略。

当同一图层中存在透视时，将始终忽略修饰符`res=`。 为图像图层指定时，将忽略修饰符`size=`。 具有`perspective=`的层中的修饰符`size=`和`res=`已保留供将来使用。

## 默认 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`，无透视转换。

## 另请参阅 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ， [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065)， [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)， [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
