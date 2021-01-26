---
description: 按名称选择对象。 按名称选择指定的暗角组，并开始新MSS。
seo-description: 按名称选择对象。 按名称选择指定的暗角组，并开始新MSS。
seo-title: obj
solution: Experience Manager
title: obj
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---


# obj{#obj}

按名称选择对象。 按名称选择指定的暗角组，并开始新MSS。

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 名称  </span> </span> </p> </td> 
  <td class="stentry"> <p>组名称或路径／名称。 </p> </td> 
 </tr> 
</table>

可使用完全限定的组路径选择子组或单个对象(即，通过指定目标组或对象的名称，该名称前面有所有父组，以/（正斜杠）分隔。

如果未找到具有指定名称的组／对象，则执行在`attribute::OnObjFail`中指定的操作。

## 属性 {#section-9463b36e8ff74c81a70c7c2b58927430}

选择命令；MSS分隔符。 对象选择是永久的，直到选择另一个对象（具有`obj=`或`sel=`）。

组／对象路径和名称不区分大小写。

## 默认 {#section-0c322850512c4896bb551856a549440e}

当打开新暗角时，会自动选择包含可渲染对象的暗角中的第一组。

## 另请参阅 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [属性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
