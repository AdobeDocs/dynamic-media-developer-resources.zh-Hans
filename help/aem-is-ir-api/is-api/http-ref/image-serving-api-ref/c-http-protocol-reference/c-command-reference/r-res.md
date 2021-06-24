---
description: 基于分辨率的图像缩放。 将图像缩放为请求的分辨率。
solution: Experience Manager
title: res
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 1%

---

# res{#res}

基于分辨率的图像缩放。 将图像缩放为请求的分辨率。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>目标分辨率；通常以每英寸像素为单位（实数）。 </p> </td> 
 </tr> 
</table>

比例因子是用&#x200B;*`val`*&#x200B;除以`catalog::Resolution`计算的。 请注意，此命令不影响回复图像的打印分辨率。

要使用此功能，必须已知原始源图像的分辨率并在`catalog::Resolution`中进行设置。 分辨率单位可能因应用程序而异。 对于可重复的2D纹理或材料色板（如壁纸或织物），分辨率可以以像素/英寸或像素/毫米表示。 航拍照片和地图可以更好地以像素/英里或像素/公里的方式提供。 无论如何，用于`catalog::Resolution`的单位必须与用于`res=`的单位相同。

除了以精确分辨率获得图像外，`res=`还可用于以相同分辨率组合多幅图像，以便这些图像中可见的项目彼此成准确比例。

>[!NOTE]
>
>通常，在将复合图像返回到客户端之前，会将其调整为目标视图大小（由`wid=`、`hei=`或`attribute::DefaultPix`指定）。 要阻止调整此大小并获得由`res=`指定的精确分辨率的图像，可能需要通过显式指定`scl=1`来禁用视图缩放。 这会指示服务器将复合图像裁剪为目标视图大小，而不是缩放该图像。

## 属性 {#section-fdbd16e59cff4952a3717146bc91412e}

源图像/蒙版属性。 被未与源图像或蒙版关联的图层忽略。 为`layer=comp`指定了应用于层0。 如果为同一层指定了`scale=`或`size=`，则忽略。

## 默认 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

如果未指定，`scale=`或`size=`将确定缩放因子，或者，如果未指定缩放因子，则使用图像而不进行缩放。

## 示例 {#section-eb06f333e08e4247971fb1b18922597b}

以12像素/英寸的对象分辨率检索纹理图像，以用于“图像渲染”或“图像创作”。 我们指定了无丢失的PNG格式和更优质的重新取样，以获得尽可能高的质量，

` http:// *`伺服器`*/myTexture?res=12&fmt=png&resMode=sharp`

## 另请参阅 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
