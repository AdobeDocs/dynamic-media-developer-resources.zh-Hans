---
description: 将提供的URL列表转发到Dynamic Media CDN（内容分发网络）提供程序，以使其现有的HTTP响应缓存失效。
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 4%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

将提供的URL列表转发到Dynamic Media CDN（内容分发网络）提供程序，以使其现有的HTTP响应缓存失效。

## cdnCacheInvalidation:关于 {#section-4f70d2bc79d64288b961836ab17e9690}

通过CDN网络处理CDN缓存失效请求后，强制针对Dynamic Media网络上当前已发布的数据，对这些URL的所有HTTP请求重新验证。 如果任何URL未连接到Dynamic Media服务URL结构，并且与创建公司时分配的Dynamic Media公司根ID直接匹配，则会导致整个请求出现API错误。 如果CDN不支持且认为无效的任何无效URL，则也会导致整个请求出现API错误。

**使用频率：规则**

控制此功能使用频率的规则由Dynamic Media的CDN合作伙伴控制。 CDN可自行决定如何降低这些无效的响应速度，以保持其服务对用户的最佳性能。 如果Dynamic Media收到过度使用此功能的通知，我们需要针对每个公司或在整个服务中完全禁用此功能。

**确认电子邮件**

来自Dynamic Media CDN合作伙伴的确认电子邮件可发送给列表的创建者，或最多5个其他电子邮件地址。 当通知整个CDN网络已清除电子邮件中引用的URL时，API会发送确认消息。 如果提供的URL数量超过Dynamic Media在单次通知中向CDN合作伙伴交付的URL数量，则对`cdnCacheInvalidation`的单次调用可以发送多封电子邮件。 目前，如果请求超过100个URL，但可能会根据CDN合作伙伴的请求进行更改，则为上述情况。

**支持时间**

6.0

## 授权用户类型 {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## 参数 {#section-bd1ed2b7419945d19a2ebd5668499f72}

**输入** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 名称</b> </th> 
   <th class="entry"> <b> 类型</b> </th> 
   <th class="entry"> <b> 必需</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 与URL连接的公司要失效的句柄。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 类型：UrlArray</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 要从CDN缓存失效的最多1000个URL的列表。 所有URL都必须包含要失效的Dynamic Media公司根ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 名称</b> </th> 
   <th class="entry"> <b> 类型</b> </th> 
   <th class="entry"> <b> 必需</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>引用清除请求的句柄。 </p> <p><span class="codeph"> cdnCacheInvalidation</span> API现在几乎立即使缓存失效（约5秒）。 因此，通常不再需要轮询失效状态。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>完成清除请求的预计秒数。 客户端应等待此时间才能轮询状态。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-f414361a58e84dfcbbac30a358d02125}

此示例请求在CDN缓存中使四个URL失效。 响应包含操作成功的概要计数以及直接从CDN提供的用于帮助客户端使用此功能的错误详细信息列表。

`getCdnCacheInvalidationStatus` 操作.

**请求**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**响应**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```
