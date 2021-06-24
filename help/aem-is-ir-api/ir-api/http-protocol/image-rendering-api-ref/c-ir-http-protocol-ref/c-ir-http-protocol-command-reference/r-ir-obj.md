---
description: 按名称选择对象。 按名称选择指定的晕影组并启动新的MSS。
solution: Experience Manager
title: obj
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---

# obj{#obj}

按名称选择对象。 按名称选择指定的晕影组并启动新的MSS。

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>组名称或路径/名称。 </p> </td> 
 </tr> 
</table>

子组或单个对象可以使用完全限定的组路径来选择(即，通过指定目标组或对象的名称，该对象前面有所有父组，以/（正斜杠）分隔。

如果未找到具有指定名称的组/对象，则执行`attribute::OnObjFail`中指定的操作。

## 属性 {#section-9463b36e8ff74c81a70c7c2b58927430}

选择命令；MSS分隔符。 对象选择将持续存在，直到选择了另一个对象（无论是使用`obj=`还是`sel=`）。

组/对象路径和名称不区分大小写。

## 默认 {#section-0c322850512c4896bb551856a549440e}

当打开新晕影时，会自动选择包含可渲染对象的晕影中的第一组。

## 另请参阅 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)，属 [性：:OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
