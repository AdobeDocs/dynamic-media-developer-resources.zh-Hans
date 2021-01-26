---
description: 按像素位置选择对象。
seo-description: 按像素位置选择对象。
seo-title: sel
solution: Experience Manager
title: sel
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# sel{#sel}

按像素位置选择对象。

` sel= *`木`*, *``*[, *`层`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y  </span> </p> </td> 
  <td class="stentry"> <p>以像素(int, int)为单位选取位置坐标。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 级别 </span> </p> </td> 
  <td class="stentry"> <p>组级别(int)。 </p> </td> 
 </tr> 
</table>

在&#x200B;*`x, y`*&#x200B;指定的像素坐标处选择组或对象，并开始新的MSS。 如果挑库位置没有可选对象，或者挑库位置无效，则执行`attribute::OnFailSel`指定的操作。

*`level`* 指定是选择最外面的组，还是向下钻取到嵌套的组或对象。如果未指定&#x200B;*`level`*，则选择最外面的组。 设置为1可在最外面的组下选择一个组级别。 设置为大数（如99）以选择最内层的可选对象或组。

## 属性 {#section-8f27e84d88734a62a5e398e0c9972bdc}

选择命令；MSS分隔符。 对象选择是永久的，直到选择另一个对象（具有`obj=`或`sel=`）。

*`x, y`* 必须在0、0（图像的左上角）到-1、-1(图 *`wid`*&#x200B;像的 *`hei`*&#x200B;右下角)的范围内，其中和是未缩 *`wid`* 放暗角 *`hei`* 视图的大小。

如果指定，*`level`*&#x200B;必须为0或更大。

## 默认 {#section-e13c705a3e76468894b4ec190ed8a893}

*`x, y`*&#x200B;为无。 *`level`* 默认值为0。

## 另请参阅 {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) wid= [,](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)hei=，属性 [::](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)DefaultPix [,](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) [属性：:OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
