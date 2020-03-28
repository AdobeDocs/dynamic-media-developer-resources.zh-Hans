---
description: 基于分辨率的图像缩放。 将图像缩放到所请求的分辨率。
seo-description: 基于分辨率的图像缩放。 将图像缩放到所请求的分辨率。
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# res{#res}

基于分辨率的图像缩放。 将图像缩放到所请求的分辨率。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>目标决议；通常以每英寸像素数（实数）为单位。 </p> </td> 
 </tr> 
</table>

比例因子是通过除以 *`val`* 计算 `catalog::Resolution`的。 请注意，此命令不会影响回复图像的打印分辨率。

要使用此功能，必须知道并设置原始源图像的分辨率 `catalog::Resolution`。 分辨率单位可能因应用程序而异。 对于可重复的2D纹理或材料色板（如墙纸或织物），分辨率可以表示为像素／英寸或像素／毫米。 航拍照片和地图可以更好地按像素／英里或像素／公里提供。 无论如何，用于的单 `catalog::Resolution` 位必须与用于的单位相同 `res=`。

除了以精确的分辨率获取图像外，还可以使用同一分辨率的多个图像来合并图像，以便这些图像中可见的项目彼此精确成比例。 `res=`

>[!NOTE]
>
>通常，在将复合图像返回到客户端之前，会将其调整为目标视图大 `wid=`小(由 `hei=`、 `attribute::DefaultPix`或指定)。 要防止这种调整大小和获得具有指定的精确分辨率的图像，可 `res=`能需要通过显式指定禁用视图缩放 `scl=1`。 这会指示服务器将合成图像裁剪为目标视图大小，而不是缩放它。

## 属性 {#section-fdbd16e59cff4952a3717146bc91412e}

源图像／蒙版属性。 被未与源图像或蒙版关联的图层忽略。 为指定了应用于图层0的 `layer=comp`内容。 如果为同一 `scale=` 层指定 `size=` 或指定了，则忽略。

## 默认 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

如果未指定， `scale=` 或确 `size=` 定缩放因子，或者，如果未指定，则不使用缩放来使用图像。

## 示例 {#section-eb06f333e08e4247971fb1b18922597b}

以12像素／英寸的对象分辨率检索纹理图像，以便与“图像渲染”或“图像创作”一起使用。 我们指定无损的PNG格式和更好的质量重新取样，以获得最佳质量，

` http:// *`伺服器`*/myTexture?res=12&fmt=png&resMode=sharp`

## 另请参阅 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog:::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
