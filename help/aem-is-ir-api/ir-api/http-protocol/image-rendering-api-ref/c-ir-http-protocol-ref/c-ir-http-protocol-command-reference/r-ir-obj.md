---
title: 对象
description: 按名称选择对象。 按名称选择指定的晕影组并启动新的MSS。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# 对象{#obj}

按名称选择对象。 按名称选择指定的晕影组并启动新的MSS。

` obj= *`名称`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>组名或路径/名称。 </p> </td> 
 </tr> 
</table>

可以使用完全限定的组路径选择子组或单个对象(即，通过指定所有父组前面以/（正斜杠）分隔的目标组或对象的名称)。

如果未找到具有指定名称的组/对象，则在 `attribute::OnObjFail` 已获取。

## 属性 {#section-9463b36e8ff74c81a70c7c2b58927430}

选择命令；MSS分隔符。 对象选择将一直保留，直到选择另一个对象(使用 `obj=` 或 `sel=`.

组/对象路径和名称不区分大小写。

## 默认 {#section-0c322850512c4896bb551856a549440e}

打开新晕影时，将自动选择晕影中包含可渲染对象的第一个组。

## 另请参阅 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)， [attribute：：OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
