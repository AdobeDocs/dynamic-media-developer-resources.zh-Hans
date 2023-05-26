---
description: 基于分辨率的图像缩放。 将图像缩放到所需分辨率。
solution: Experience Manager
title: res
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# res{#res}

基于分辨率的图像缩放。 将图像缩放到所需分辨率。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>目标分辨率；通常以像素/英寸（实际）为单位。 </p> </td> 
 </tr> 
</table>

比例因子通过除法来计算 *`val`* 作者： `catalog::Resolution`. 请注意，此命令不会影响回复图像的打印分辨率。

要使用此功能，必须知道原始源图像的分辨率并在中进行设置 `catalog::Resolution`. 根据应用的不同，分辨率单位可能有所不同。 对于可重复的2D纹理或材料色板（如墙纸或织物），分辨率可以表示为像素/英寸或像素/毫米。 航拍照片和地图可能以像素/英里或像素/公里为单位提供更好的服务。 无论如何，使用的单位 `catalog::Resolution` 必须与使用的单位相同 `res=`.

除了获得精确分辨率的图像之外， `res=` 还可用于组合具有相同分辨率的多个图像，以使这些图像中可见的项目彼此保持准确比例。

>[!NOTE]
>
>通常，复合图像会调整到目标视图大小（由指定） `wid=`， `hei=`，或 `attribute::DefaultPix`)，然后将其返回到客户端。 要防止这种调整大小操作，并获取分辨率由指定的图像 `res=`中，可能需要通过显式指定来禁用视图缩放 `scl=1`. 这会指示服务器将复合图像裁剪为目标视图大小，而不是缩放它。

## 属性 {#section-fdbd16e59cff4952a3717146bc91412e}

源图像/蒙版属性。 被与源图像或蒙版无关的图层忽略。 指定应用于层0 `layer=comp`. 在以下情况下忽略： `scale=` 或 `size=` 为同一层指定。

## 默认 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

如果未指定， `scale=` 或 `size=` 确定缩放因子，如果未指定缩放因子，则使用图像而不进行缩放。

## 示例 {#section-eb06f333e08e4247971fb1b18922597b}

检索对象分辨率为12像素/英寸的纹理图像，以用于图像渲染或图像创作。 我们指定无损失PNG格式和质量更好的重新取样，以获得最佳质量，

` http:// *`伺服器`*/myTexture?res=12&fmt=png&resMode=sharp`

## 另请参阅 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog：：Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ， [attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
