---
title: 提供静态（非图像）内容
description: 您可以使用图像服务管理目录中的非图像内容，并通过单独的/is/content上下文提供该内容。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# 提供静态（非图像）内容{#serving-static-non-image-contents}

您可以使用图像服务管理目录中的非图像内容，并通过单独的/is/content上下文提供该内容。

此功能允许分别为每个项目配置TTL。

图像服务支持以下命令： [!DNL /is/content]：

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> 类型 </a> </p> </td> 
  <td class="stentry"> <p>内容类型过滤器。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> 需要 </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>， <span class="codeph"> req=props </span>、和 <span class="codeph"> req=exists </span> 仅限。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> 缓存 </a> </p> </td> 
  <td class="stentry"> <p>允许禁用客户端缓存。 </p> </td> 
 </tr> 
</table>

## 基本语法 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 请求 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> 服务器 </span>/is/content[/catalog/ <span class="varname"> 项目 </span>][？ <span class="varname"> 修饰符 </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 服务器 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ ： <span class="varname"> 端口 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 目录 </span> </span> </p> </td> 
  <td class="stentry"> <p>目录标识符。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 项目 </span> </span> </p> </td> 
  <td class="stentry"> <p>静态内容项ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修饰符 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span>*[&amp; <span class="varname"> 命令 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> 值 </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>支持的命令名称之一。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> catalog：：Id </span> </p> </td> 
   <td colname="col2"> <p>此静态内容项的目录记录标识符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：Path </span> </p> </td> 
   <td colname="col2"> <p>此内容项的文件路径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：过期时间 </span> </p> </td> 
   <td colname="col2"> <p>此内容项的TTL； <span class="codeph"> attribute：：Expiration </span> 如果未指定或为空，则使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：时间戳 </span> </p> </td> 
   <td colname="col2"> <p>文件修改时间戳；在通过启用基于目录的验证时需要 <span class="codeph"> attribute：：CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：UserData </span> </p> </td> 
   <td colname="col2"> <p>与此静态内容项关联的可选元数据；可用于具有以下功能的客户端： <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog：：UserType </span> </p> </td> 
   <td colname="col2"> <p>可选数据类型；可用于筛选对静态内容的请求 <span class="codeph"> type=命令 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 过滤静态内容 {#section-4c41bf41ff994910840c1352683d1f37}

此机制有助于确保客户端仅接收适合其需求的内容。 假定静态内容使用适当的进行标记 `catalog::UserType` 值，客户端可以添加 `type=` 命令到请求。 图像服务将提供的值与 `type=` 命令到值 `catalog::UserType` 如果不匹配，将返回错误，而不是返回可能不适当的内容。

## 视频字幕文件 {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

您可以封装视频字幕文件(WebVTT)、CSS或JSONP格式的任何文本文件。 JSON响应描述如下。

* 对于WebVTT文件，响应的mime类型为text/javascript。 不返回JSON；而是返回使用JSON调用方法的JavaScript。 ID和处理程序都是可选的。
* 对于CSS文件，响应的mime类型为text/javascript。 ID和处理程序都是可选的。
* 默认情况下，会应用UTF-8编码以确保正确对其进行解码。 默认大小限制为2 MB。

您还可以将跟踪用于其他类型的定时元数据。 每个轨道元素的源数据是一个由定时提示列表组成的文本文件。 提示可以包括JSON或CSV等格式的数据。

请参阅 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) 有关JSONP格式的详细信息。

请参阅 [www.json.org](https://www.json.org/json-en.html) 以了解有关JSON格式的详细信息。

## 另请参阅 {#section-7b28631016044a22a3a6762fd64771e9}

[类型=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ， [需要=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [图像目录引用](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
