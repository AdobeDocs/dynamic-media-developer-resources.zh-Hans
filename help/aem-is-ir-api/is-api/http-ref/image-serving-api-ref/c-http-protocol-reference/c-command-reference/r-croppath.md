---
description: 允许您裁剪到嵌入的命名路径的定界框。 此裁切反过来会更改图像的大小。
seo-description: 允许您裁剪到嵌入的命名路径的定界框。 此裁切反过来会更改图像的大小。
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# cropPathE{#croppathe}

允许您裁剪到嵌入的命名路径的定界框。 此裁切反过来会更改图像的大小。

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>嵌入在图层源图像中的路径名称（仅限ASCII）。 </p> <p> <span class="codeph"><span class="varname"> </span></span> pathName是嵌入在图层源图像中的路径的名称。根据需要自动变换路径以保持与图像内容的相对对齐。 如果指定了多个<span class="codeph"><span class="varname"> pathName</span></span>，则服务器会裁切到每个路径的边框，一次裁切一个。 将忽略源映像中未找到的任何<span class="codeph"><span class="varname"> pathName</span></span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

图层属性。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果图层忽略。

`cropPathE=` 如果在图层源图像中未找到具有指定名称的路径，或者图层源不是图像，则忽略该路径。

## 默认 {#section-d1986aa31af14767aeb1b4a57add67f4}

“无”，不用于图层的其他裁剪。

## 另请参阅 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[crop](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
