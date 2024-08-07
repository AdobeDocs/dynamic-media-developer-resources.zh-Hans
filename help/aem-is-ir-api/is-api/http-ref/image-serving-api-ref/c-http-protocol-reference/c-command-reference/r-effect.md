---
title: 效果
description: 选择“效果图层”。 选择一个效果层，并在请求字符串中启动一个与当前层关联的新层段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# 效果{#effect}

选择“效果图层”。 选择一个效果层，并在请求字符串中启动一个与当前层关联的新层段。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>效果图层编号（int不等于0）。 </p></td> 
 </tr> 
</table>

新段中的所有命令都应用于指定的效果层。 下一个`layer=`或`effect=`命令或请求结束时终止效果层区段。

对于外层效果（即父层后的效果），值&#x200B;*`n`*&#x200B;必须小于0；对于内层效果（即父层内的效果），值必须大于0。 效果图层编号不必是连续的。

如果同一父层有多个效果层，则效果层编号指定z顺序。 编号较高的图层位于编号较低的图层之上。

效果层可以附加到`layer=comp`。

## 属性 {#section-e11f795deff345779ce280a82cf221ca}

效果层命令。 值&#x200B;*`n`*&#x200B;不能为0。

## 默认 {#section-84bbe1cfe7a94040827c994323ac59d4}

无。

## 示例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 另请参阅 {#section-573273e9e0e64103a5764075f5e50180}

[图层=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
