---
description: 您可以使用“图像提供”来管理目录中的非图像内容，并通过单独的/is/content上下文提供该内容。
solution: Experience Manager
title: 提供静态（非图像）内容
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# 提供静态（非图像）内容{#serving-static-non-image-contents}

您可以使用“图像提供”来管理目录中的非图像内容，并通过单独的/is/content上下文提供该内容。

此功能允许单独配置每个项的TTL。

图像服务支持[!DNL /is/content]中的以下命令：

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> 类型 </a> </p> </td> 
  <td class="stentry"> <p>内容类型过滤器。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> 请求  </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>、  <span class="codeph"> req=prop  </span>和req= <span class="codeph"> exists(仅存 </span> 在)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> 缓存  </a> </p> </td> 
  <td class="stentry"> <p>允许禁用客户端缓存。 </p> </td> 
 </tr> 
</table>

## 基本语法 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 请求  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http://  <span class="varname"> server  </span>/is/content[/catalog/  <span class="varname"> item  </span>][?<span class="varname"> 修饰符 </span>]  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 服务器  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ : <span class="varname"> 端口 </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 目录  </span> </span> </p> </td> 
  <td class="stentry"> <p>目录标识符。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 项目  </span> </span> </p> </td> 
  <td class="stentry"> <p>静态内容项ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修饰语  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span>*[&amp; <span class="varname"> 命令 </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> value  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>支持的命令名称之一。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>命令值。 </p> </td> 
 </tr> 
</table>

## 静态内容目录 {#section-91014f17f0d543d7aaf24539b2d7d4b9}

静态内容目录与图像目录类似，但支持的数据字段较少：

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性/数据 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目录：:Id  </span> </p> </td> 
   <td colname="col2"> <p>此静态内容项目的目录记录标识符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目录：：路径  </span> </p> </td> 
   <td colname="col2"> <p>此内容项的文件路径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目录：：过期  </span> </p> </td> 
   <td colname="col2"> <p>此内容项的TTL;<span class="codeph">属性：如果未指定或为空，则使用过期</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>文件修改时间戳；启用<span class="codeph">属性：:CacheValidationPolicy </span>的基于目录的验证时需要此参数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td colname="col2"> <p>与此静态内容项目关联的可选元数据；适用于具有<span class="codeph"> req=userdata </span>的客户端。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType  </span> </p> </td> 
   <td colname="col2"> <p>可选数据类型；可以使用<span class="codeph"> type=命令</span>筛选静态内容的请求。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 筛选静态内容 {#section-4c41bf41ff994910840c1352683d1f37}

此机制有助于确保客户端仅接收适合其需求的内容。 假设静态内容已使用相应的`catalog::UserType`值进行标记，则客户端可以向请求添加`type=`命令。 图像服务将`type=`命令提供的值与`catalog::UserType`的值进行比较，如果不匹配，则返回错误，而不是可能不适当的内容。

## 视频标题文件 {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

您可以以JSONP格式封装视频标题文件(WebVTT)、CSS或任何文本文件。 JSON响应的描述如下。

* 对于WebVTT文件，响应的mime类型为text/javascript。 未返回JSON;而是会返回使用JSON调用方法的Javascript。 ID和处理程序都是可选的。
* 对于CSS文件，响应的mime类型为text/javascript。 ID和处理程序都是可选的。
* 默认情况下，会应用UTF-8编码来确保正确解码。 默认大小限制为2 MB。

您还可以将跟踪用于其他类型的定时元数据。 每个跟踪元素的源数据是由定时提示列表组成的文本文件。 提示可以包含JSON或CSV等格式的数据。

有关JSONP格式的更多信息，请参阅[http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP)。

有关JSON格式的更多信息，请参阅[www.json.org](http://www.json.org)。

## 另请参阅 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Image Catalog  [Reference](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
