---
title: 裁切路径E
description: 允许您裁切到嵌入命名路径的边界框。 此裁剪会依次更改图像的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---

# 裁切路径E{#croppathe}

允许您裁切到嵌入命名路径的边界框。 此裁剪会依次更改图像的大小。

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>嵌入到图层源图像中的路径的名称（仅限ASCII）。 </p> <p> <span class="codeph"><span class="varname"> pathName</span></span>是嵌入到图层源图像中的路径的名称。 根据需要自动转换路径以保持与图像内容的相对对齐。 如果指定了多个<span class="codeph"><span class="varname"> pathName</span></span>，服务器将裁剪到每个路径的边界框，一次裁剪一个。 在源映像中未找到任何<span class="codeph"><span class="varname"> pathName</span></span>将被忽略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

层属性。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果层忽略。

如果在图层源映像中未找到具有指定名称的路径，或者图层源不是映像，则忽略`cropPathE=`。

## 默认 {#section-d1986aa31af14767aeb1b4a57add67f4}

无，表示没有附加的图层裁剪。

## 另请参阅 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[裁切](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)，[clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
