---
description: 请求规则元素。 在<ruleset>元素中，一个或多个规则是可选的。
seo-description: 请求规则元素。 在<ruleset>元素中，一个或多个规则是可选的。
seo-title: 规则
solution: Experience Manager
title: 规则
uuid: 8b8e5b06-a0b7-47e1-942d-0297d08c313b
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 6%

---


# 规则{#rule}

请求规则元素。 在`<ruleset>`元素中，一个或多个规则是可选的。

## 属性 {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"`: 可选. 默认为“break”。

`Replace = "first" | "all"`: 可选. 默认为“first”。

`RequestType` =  *&quot;`types`*:可选。指定规则应用于的输入上下文。 *`types`* 是逗号分隔的列表，其中可能包括下表中列出的一个或多个令牌。如果未指定`RequestType`，则此规则适用于在所有支持的上下文上接收的请求。

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>令牌</b> </p> </th> 
   <th class="entry"> <p><b>上下文</b> </p> </th> 
   <th class="entry"> <p><b>说明</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 是</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>应用于图像服务请求 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>应用于图像渲染请求 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 静态</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>应用于静态内容请求 </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`**: 可选. 用于标识调试日志和错误消息中的`<rule>`元素。

`  *`属性`* ="value"`:可选。`<rule>` 元素可以在任意组合中定义以下任意属性。如果指定，并且规则成功匹配，则它们将覆盖此请求的相应目录属性。 默认值为 `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> 属性  </span> </b> </th> 
   <th class="entry"> <p>相应的图像目录属性 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> 属性：:DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> 属性：:ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 过期时间</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> 属性：:Expiration</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> 属性：:MaxPix  </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> attribute::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 请求模糊处理</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> attribute::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> attribute::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> 属性：:SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 水印</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> 属性：:WaterMark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

有关详细信息，请参阅相应图像目录属性的说明。

过期属性只覆盖默认属性值。 如果特定的`catalog::Expiration`值应用于请求，则忽略覆盖。

## 数据 {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>可选 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
  <td class="stentry"> <p>可选 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span> </p></td> 
  <td class="stentry"> <p>可选 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;header&gt;</span> </p></td> 
  <td class="stentry"> <p>可选 </p></td> 
 </tr> 
</table>

## 说明 {#section-0c5fbc363070419d8c9800b0c02dc9f9}

如果同时指定了`<expression>`和`<substitution>`，并且未使用捕获的子字符串，则第一个匹配的子字符串将替换为`<substitution>`。

如果未指定`<expression>`，则任何路径匹配，并将`<substitution>`附加到路径末尾。

如果未指定`<substitution>`，则不会发生路径或查询转换，但会覆盖任何指定的目录属性。 如果`<substitution>`为空，则删除匹配的子字符串。

`<addressfilter>`仅在发生匹配时和应用查询规则之前应用。
