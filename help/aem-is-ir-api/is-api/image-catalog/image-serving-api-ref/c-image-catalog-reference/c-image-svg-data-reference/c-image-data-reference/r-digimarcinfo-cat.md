---
description: Digimarc图像信息。 启用Digimarc嵌入并指定水印类型和任何关联的特定图像数据。
seo-description: Digimarc图像信息。 启用Digimarc嵌入并指定水印类型和任何关联的特定图像数据。
seo-title: DigimarcInfo
solution: Experience Manager
title: DigimarcInfo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8371880e-47df-4333-b8a6-91feaf16c409
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 13%

---


# DigimarcInfo{#digimarcinfo}

Digimarc图像信息。 启用Digimarc嵌入并指定水印类型和任何关联的特定图像数据。

## 属性 {#section-62af219e8bac422b8541841221c9ce4f}

四个整数值，用逗号分隔。

`*``*, *``*, *`typeflagsval1`*, *`val2`*`

`*``*` typeenables Digimarc嵌入并指定水印类型：

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 类型</span> </span> </p> </th> 
   <th class="entry"> <p><b>水印类型</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>基本. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>图像 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>交易 ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>版权年份。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`标`*` 出一个具有三个值的位字段。设置位0以指示受复制保护的内容，设置位1以指示受限内容，设置位2以指示成人内容：

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 标志</span> </span> </p> </th> 
   <th class="entry"> <p><b>说明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>受复制保护。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>受限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>受复制保护，受限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>成熟的内容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>复制受保护的成人内容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>受限的成人内容。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>受复制保护、受限、成熟的内容。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`val1`*`和`*`val2`*`的解释取决于`*`类型`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> 类型</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>未使用。 </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>图像 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>交易 ID. </p> </td> 
   <td> <p>未使用。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>第一个版权年。 </p> </td> 
   <td> <p>第二个版权年。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 默认 {#section-4bb97e5f79074be89cc691e73449eb43}

继承自属性：:DigimarcInfo（如果字段不存在或为空）。

## 示例 {#section-0f14727a0a2a408781c9df71fed7f42d}

“0,0,0,0”将禁用此图像的Digimarc水印。

“1,5,0,0”指定设置了成人和受复制保护的内容标志的基本水印。

“2,0,4567,0”指定带有图像ID的水印。

“3,2,56483,0”指定具有事务ID和受限内容标志设置的水印。

“4,0,1998,2001”指定了版权年的水印。

## 另请参阅 {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[属性：:DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [属性：:DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
