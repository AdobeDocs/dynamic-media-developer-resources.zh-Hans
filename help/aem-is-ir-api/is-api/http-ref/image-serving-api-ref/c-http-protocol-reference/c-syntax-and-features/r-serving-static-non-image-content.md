---
description: 提供静态（非图像）内容
solution: Experience Manager
title: 提供静态（非图像）内容
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 提供静态（非图像）内容{#serving-static-non-image-content}

图像服务提供了一种机制，用于管理目录中的非图像内容，并通过单独的`context /is/content`提供该内容。 该机制允许分别为每个项目配置TTL。

## 基本语法 {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">请求</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname">服务器</span>/is/content[/ <span class="varname">目录</span>/ <span class="varname">项</span>][？ <span class="varname">修饰符</span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">服务器</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">服务器地址</span>[： <span class="varname">端口</span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">目录</span> </span> </p> </td> 
  <td class="stentry"> <p>目录标识符。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">项目</span> </span> </p> </td> 
  <td class="stentry"> <p>静态内容项ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">修饰符</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">命令</span>*[&amp; <span class="varname">命令</span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">命令</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname">值</span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>支持的命令名称之一。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
  <td class="stentry"> <p>命令值。 </p> </td> 
 </tr> 
</table>

## 命令概述 {#section-61657a0141914053ab12038ad7e91500}

图像服务支持位于/is/content的以下命令：

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local">类型</a> </td> 
  <td class="stentry"> <p>内容类型过滤器。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local">请求</a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>、<span class="codeph"> req=props </span>和<span class="codeph"> req=exists </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local">缓存</a> </td> 
  <td class="stentry"> <p>允许禁用客户端缓存。 </p> </td> 
 </tr> 
</table>

## 静态内容目录 {#section-b2b8f4860fe84e528493ed704c7c5141}

静态内容目录与图像目录类似，但支持的数据字段较少：

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>属性/数据</b> </th> 
   <th class="entry"> <b>备注</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：Id </span> </p> </td> 
   <td> <p> 此静态内容项的目录记录标识符 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：路径</span> </p> </td> 
   <td> <p> 此内容项的文件路径 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：过期</span> </p> </td> 
   <td> <p> 如果未指定或为空，则使用此内容项目的TTL；attribute：：Expiration </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：时间戳</span> </p> </td> 
   <td> <p> 文件修改时间戳；使用attribute：：CacheValidationPolicy启用基于目录的验证时需要 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：UserData </span> </p> </td> 
   <td> <p> 与此静态内容项关联的可选元数据；对于具有req=userdata的客户端可用 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">目录：：UserType </span> </p> </td> 
   <td> <p> 可选数据类型；可用于通过type=命令筛选静态内容的请求 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 过滤静态内容 {#section-896c37cf68bc446eb0766fb378898262}

此机制有助于确保客户端仅接收适合其需求的内容。 假定静态内容已使用适当的`catalog::UserType`值标记，则客户端可以将`type=`命令添加到请求中。 图像服务将随`type=`命令提供的值与`catalog::UserType`的值进行比较，如果不匹配，则返回错误而非可能不适当的内容。

## 另请参阅 {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[类型=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb)，[请求=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)，[图像目录引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
