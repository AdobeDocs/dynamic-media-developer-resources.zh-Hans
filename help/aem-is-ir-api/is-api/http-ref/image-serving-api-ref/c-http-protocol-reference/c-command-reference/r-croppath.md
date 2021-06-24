---
description: 用于裁切到嵌入的命名路径的定界框。 此裁剪反过来会更改图像的大小。
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# cropPathE{#croppathe}

用于裁切到嵌入的命名路径的定界框。 此裁剪反过来会更改图像的大小。

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>层源图像中嵌入的路径的名称（仅限ASCII）。 </p> <p> <span class="codeph"><span class="varname"> </span></span> pathName是嵌入在层源图像中的路径的名称。根据需要自动变换路径以保持与图像内容的相对对准。 如果指定了多个<span class="codeph"><span class="varname"> pathName</span></span>，则服务器会裁剪到每个路径的定界框，每次一个。 在源映像中找不到的任何<span class="codeph"><span class="varname"> pathName</span></span>都将被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

层属性。 应用于当前层或复合图像（如果`layer=comp`）。 被效果层忽略。

`cropPathE=` 如果在层源图像中未找到具有指定名称的路径，或者层源不是图像，则忽略该路径。

## 默认 {#section-d1986aa31af14767aeb1b4a57add67f4}

“无”(None)，表示不会再裁剪图层。

## 另请参阅 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[裁剪](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
