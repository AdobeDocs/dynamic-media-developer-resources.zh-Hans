---
description: 反轉的圖層剪裁路徑。 指定目前圖層的排除剪裁路徑。 在clipXPath=所定義區域內的任何圖層部分都會呈現為透明。
solution: Experience Manager
title: clipXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d7e92f5-856f-4d62-a5d3-4726d7b43792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# clipXPath{#clipxpath}

反轉的圖層剪裁路徑。 指定目前圖層的排除剪裁路徑。 在clipXPath=所定義區域內的任何圖層部分都會呈現為透明。

`clipXPath= *`pathDefinition`*`

`clipXPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路徑資料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>內嵌在圖層來源影像中的路徑名稱（僅限ASCII）。 </p></td> 
 </tr> 
</table>

另請參閱 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 以取得其他資訊，包括 `*`pathName`*` 和 `*`pathDefinition`*`.

## 屬性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

圖層屬性。 套用至目前圖層或複合影像，如果 `layer=comp`. 忽略條件 `clipPath=` 未指定。 被效果圖層忽略。

## 默认 {#section-d1986aa31af14767aeb1b4a57add67f4}

无。

## 另请参阅 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
