---
description: 选择“效果图层”。 选择一个效果层，并在请求字符串中启动与当前层关联的新层段。
solution: Experience Manager
title: 效果
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# 效果{#effect}

选择“效果图层”。 选择一个效果层，并在请求字符串中启动与当前层关联的新层段。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>效果图层编号（整数不等于0）。 </p></td> 
 </tr> 
</table>

新段内的所有命令都应用于指定的效果层。 效果层段由下一个`layer=`或`effect=`命令或请求结束终止。

*`n`* 对于外层效果（即父层后的效果），必须小于0；对于内层效果（即父层内的效果），必须大于0。效果图层编号不必是连续的。

当同一父层有多个效果层时，效果层编号会指定z顺序。 较高编号的图层放置在较低编号的图层的顶部。

效果层可附加到`layer=comp`。

## 属性 {#section-e11f795deff345779ce280a82cf221ca}

效果层命令。 *`n`* 不得为0。

## 默认 {#section-84bbe1cfe7a94040827c994323ac59d4}

无。

## 示例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 另请参阅 {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
