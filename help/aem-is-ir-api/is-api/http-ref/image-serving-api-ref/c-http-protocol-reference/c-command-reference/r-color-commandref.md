---
title: 颜色
description: 图层颜色。 指定纯色和效果图层的前景色和不透明度，以及文本图层的文本框填充颜色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 3%

---

# 颜色{#color}

图层颜色。 指定纯色和效果图层的前景色和不透明度，以及文本图层的文本框填充颜色。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 颜色 </span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK颜色值，无论是否有Alpha。 </p> </td> 
 </tr> 
</table>

如果有图像和文本图层， `color=` 在*之前使用指定的颜色*填充图层边界矩形内的透明和半不透明区域 `rotate=` 和 `extend=` 中所有规则都适用的URL的区域。

## 属性 {#section-d6e74c36a49547849212e4db8927e678}

层属性。 应用到当前图层或图层0，如果 `layer=comp`.

修饰符 *`color`* 被假定存在于与像素类型对应的工作颜色空间中 *`color`*. 和 *`color`* 如果图层图像在合并时具有不同的像素类型，则精确转换。

## 默认 {#section-60611c72876b4c45b5c85ce35608e5ec}

纯色和效果图层没有默认值；必须指定颜色。 对于图像和文本图层，默认为0,0，0,0（完全透明）。

## 示例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在下面的模板片段中，文本背景设置为50%不透明颜色，并使用相同的颜色在图层2图像周围添加半透明10像素边框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另请参阅 {#section-f0e059f857b64b61ab4f23312b8dc619}

[颜色](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)， [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)， [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)， [扩展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)， [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)， [色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
