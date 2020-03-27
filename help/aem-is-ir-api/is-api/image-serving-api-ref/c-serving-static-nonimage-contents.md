---
description: 您可以使用图像服务管理目录中的非图像内容，并通过单独的/is/content上下文提供该内容。
seo-description: 您可以使用图像服务管理目录中的非图像内容，并通过单独的/is/content上下文提供该内容。
seo-title: 提供静态（非图像）内容
solution: Experience Manager
title: 提供静态（非图像）内容
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 提供静态（非图像）内容{#serving-static-non-image-contents}

您可以使用图像服务管理目录中的非图像内容，并通过单独的/is/content上下文提供该内容。

此功能允许单独配置每个项目的TTL。

图像服务支持以下命令： [!DNL /is/content]

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> 类型 </a> </p> </td> 
  <td class="stentry"> <p>内容类型过滤器。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、 <span class="codeph"> req=props </span>和req=exists <span class="codeph"></span> only。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> 高速缓存 </a> </p> </td> 
  <td class="stentry"> <p>允许禁用客户端缓存。 </p> </td> 
 </tr> 
</table>

## 基本语法 {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 请求 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="filepath"><span class="varname"> server/is/content[/catalog/ </span>item <span class="varname"></span>[? <span class="varname"> 修饰符 </span>] </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 服务器 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> 端 </span>口] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 目录 </span></span> </p> </td> 
  <td class="stentry"> <p>目录标识符。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 项目 </span></span> </p> </td> 
  <td class="stentry"> <p>静态内容项ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 修饰 </span> 符 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命 </span>令*[&amp;命 <span class="varname"> 令 </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 命令 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmd名称 </span></span> </p> </td> 
  <td class="stentry"> <p>支持的命令名称之一。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span></span> </p> </td> 
  <td class="stentry"> <p>命令值。 </p> </td> 
 </tr> 
</table>

## 静态内容目录 {#section-91014f17f0d543d7aaf24539b2d7d4b9}

静态内容目录与图像目录类似，但支持的数据字段较少：

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性／数据 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog:::Id </span> </p> </td> 
   <td colname="col2"> <p>此静态内容项的目录记录标识符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td colname="col2"> <p>此内容项的文件路径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 目录：:Expiration </span> </p> </td> 
   <td colname="col2"> <p>此内容项的TTL;属 <span class="codeph"> 性：:Expiration </span> is used if not specified or if empty. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>文件修改时间戳；在启用属性：:CacheValidationPolicy的基于目录的验 <span class="codeph"> 证时必需 </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>与此静态内容项关联的可选元数据；客户端可使用req= <span class="codeph"> userdata </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>可选数据类型；可以使用type=命令过滤静态内 <span class="codeph"> 容的请求 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 过滤静态内容 {#section-4c41bf41ff994910840c1352683d1f37}

此机制有助于确保客户端仅接收适合其需求的内容。 假定静态内容标记了适当的 `catalog::UserType` 值，客户端可以向请 `type=` 求添加命令。 图像服务将随命令提供的值与 `type=` 的值进行比较，如果不匹配， `catalog::UserType` 则返回错误而不是可能不适当的内容。

## 视频题注文件 {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

可以封装JSONP格式的视频题注文件(WebVTT)、CSS或任何文本文件。 JSON响应如下所述。

* 对于WebVTT文件，响应的mime类型为text/javascript。 不返回JSON;而是返回调用JSON方法的Javascript。 ID和处理函数都是可选的。
* 对于CSS文件，响应的mime类型为text/javascript。 ID和处理函数都是可选的。
* 默认情况下，应用UTF-8编码以确保正确解码。 默认大小限制为2 MB。

您还可以将轨道用于其他类型的定时元数据。 每个轨道元素的源数据是由一列表定时提示组成的文本文件。 提示可以包括JSON或CSV等格式的数据。

有关 [JSONP格式的更多信息](http://en.wikipedia.org/wiki/JSONP) ，请参阅http://en.wikipedia.org/wiki/JSONP。

有关 [JSON格式的更多信息](http://www.json.org) ，请参阅www.json.org。

## 另请参阅 {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[, Image Catalog Reference](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
