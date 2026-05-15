---
title: 对象
description: 按名称选择对象。 按名称选择指定的晕影组并启动新的MSS。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
TQID: 'https://experienceleague.adobe.com/te9iyNajxDfgvHqqThbVUc7tBItxfMtxhOMl2eCLOsk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 2%

---

# 对象{#obj}

按名称选择对象。 按名称选择指定的晕影组并启动新的MSS。

` obj= *`名称`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">名称</span> </span> </p> </td> 
  <td class="stentry"> <p>组名或路径/名称。 </p> </td> 
 </tr> 
</table>

可以使用完全限定的组路径选择子组或单个对象(即，通过指定所有父组前面以/（正斜杠）分隔的目标组或对象的名称)。

如果未找到具有指定名称的组/对象，则会执行`attribute::OnObjFail`中指定的操作。

## 属性 {#section-9463b36e8ff74c81a70c7c2b58927430}

选择命令；MSS分隔符。 对象选择是永久性的，直到选择另一个对象（带有`obj=`或`sel=`）为止。

组/对象路径和名称不区分大小写。

## 默认 {#section-0c322850512c4896bb551856a549440e}

打开新晕影时，将自动选择晕影中包含可渲染对象的第一个组。

## 另请参阅 {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b)，[attribute：：OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
