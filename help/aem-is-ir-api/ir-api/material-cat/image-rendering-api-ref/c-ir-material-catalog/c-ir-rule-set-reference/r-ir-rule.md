---
description: 请求规则元素。 <ruleset>元素中的一个或多个是可选的。
solution: Experience Manager
title: 规则
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 4%

---

# 规则{#rule}

请求规则元素。 `<ruleset>`元素中的一个或多个是可选的。

## 属性 {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"`可选。 默认值为“break”。

` Name=" *`文本`*"`可选。 用于标识调试日志和错误消息中的`<rule>`元素。

此外，`<rule>`元素可以任意组合定义以下任何属性。 如果指定并且规则匹配成功，则它们将覆盖此请求对应的目录属性。

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt;属性 </p> </th> 
   <th colname="col2" class="entry"> <p>对应的图像目录属性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local">属性：：DefautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local">属性：：ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">过期</span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local">属性：：过期</a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local">属性：：MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local">属性：：RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

有关详细信息，请参阅相应图像目录属性的描述。

Expiration属性仅覆盖默认属性值；如果特定的`catalog::Expiration`值应用于请求，则忽略该属性。

## 数据 {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;表达式&gt; </span> </p> </td> 
  <td class="stentry"> <p>可选. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;替换&gt; </span> </p> </td> 
  <td class="stentry"> <p>可选. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;地址筛选器&gt; </span> </p> </td> 
  <td class="stentry"> <p>可选. </p> </td> 
 </tr> 
</table>

## 说明 {#section-a27b91f9a03047c0bb7edc0967fb4216}

如果同时指定了`<expression>`和`<substitution>`，但未使用捕获的子字符串，则第一个匹配的子字符串将被替换为`<substitution>`。

如果未指定`<expression>`，则所有路径都将匹配，并且`<substitution>`将附加到路径的末尾。

如果未指定`<substitution>`，则将删除匹配的子字符串。

`<addressfilter>`仅在发生匹配时应用，并且是在应用查询规则之前应用。
