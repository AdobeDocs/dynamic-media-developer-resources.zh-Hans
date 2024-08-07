---
title: sel
description: 按像素位置选择对象。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%

---

# sel{#sel}

按像素位置选择对象。

` sel= *`x`*, *`y`*[, *`级别`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x，y </span> </p> </td> 
  <td class="stentry"> <p>选取以像素(int， int)为单位的位置坐标。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">级别</span> </p> </td> 
  <td class="stentry"> <p>组级别(int)。 </p> </td> 
 </tr> 
</table>

在&#x200B;*`x, y`*&#x200B;指定的像素坐标处选择组或对象并启动新的MSS。 如果领料位置没有可选对象，或者领料位置无效，则执行`attribute::OnFailSel`指定的操作。

*`level`*&#x200B;指定是选择最外部的组，还是向下钻取到嵌套组或对象。 如果未指定&#x200B;*`level`*，则选择最外部的组。 设置为1可在最外层的组下选择一个组级别。 设置为一个大数（如99）以选择最内层的可选对象或组。

## 属性 {#section-8f27e84d88734a62a5e398e0c9972bdc}

选择命令；MSS分隔符。 对象选择是永久性的，直到选择另一个对象（带有`obj=`或`sel=`）为止。

*`x, y`*&#x200B;必须在0， 0 （图像的左上角）到&#x200B;*`wid`*-1， *`hei`*-1 （图像的右下角）的范围内，其中&#x200B;*`wid`*&#x200B;和&#x200B;*`hei`*&#x200B;是未缩放晕影视图的大小。

如果指定，*`level`*&#x200B;必须大于或等于0。

## 默认 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`*&#x200B;无。 *`level`*&#x200B;默认为0。

## 另请参阅 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ，[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)，[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)，[attribute：：DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)，[attribute：：OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
