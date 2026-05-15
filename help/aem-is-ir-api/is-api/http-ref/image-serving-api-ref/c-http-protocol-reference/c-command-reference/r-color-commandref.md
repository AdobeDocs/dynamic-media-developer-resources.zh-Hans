---
title: 颜色
description: 图层颜色。 指定纯色和效果图层的前景色和不透明度，以及文本图层的文本框填充颜色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
TQID: 'https://experienceleague.adobe.com/tjiZfVTztBPgsIYS1SGtVeBxo0Wq1q8Ur-kq3Xtm6og'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 3%

---

# 颜色{#color}

图层颜色。 指定纯色和效果图层的前景色和不透明度，以及文本图层的文本框填充颜色。

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">颜色</span> </span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK颜色值，无论是否有Alpha。 </p> </td> 
 </tr> 
</table>

如果存在图像和文本图层，则在应用* `rotate=`和`extend=`之前，`color=`会用指定的颜色*填充图层边框矩形内的透明和半透明区域。

## 属性 {#section-d6e74c36a49547849212e4db8927e678}

层属性。 应用于当前图层，或应用于图层0（如果为`layer=comp`）。

假定修饰符&#x200B;*`color`*&#x200B;存在于与像素类型&#x200B;*`color`*&#x200B;对应的工作色彩空间中。 如果在合并时图层图像具有不同的像素类型，则精确转换&#x200B;*`color`*。

## 默认 {#section-60611c72876b4c45b5c85ce35608e5ec}

纯色和效果图层没有默认值；必须指定颜色。 对于图像和文本图层，默认为0,0，0,0（完全透明）。

## 示例 {#section-2d090493f4ec4e188bbc5565aa151a05}

在下面的模板片段中，文本背景设置为50%不透明颜色，并使用相同的颜色在图层2图像周围添加半透明10像素边框：

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## 另请参阅 {#section-f0e059f857b64b61ab4f23312b8dc619}

[颜色](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)，[bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)，[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)，[扩展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)，[bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)，[色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
