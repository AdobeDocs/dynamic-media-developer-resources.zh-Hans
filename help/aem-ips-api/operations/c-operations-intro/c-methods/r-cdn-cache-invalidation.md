---
description: 将提供的URL列表转发给Dynamic Media CDN（内容分发网络）提供程序，以使其现有的HTTP响应缓存失效。
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 1%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

将提供的URL列表转发给Dynamic Media CDN（内容分发网络）提供程序，以使其现有的HTTP响应缓存失效。

## cdnCacheInvalidation：关于 {#section-4f70d2bc79d64288b961836ab17e9690}

在通过CDN网络处理此失效请求后，CDN缓存失效会强制根据Dynamic Media网络上的当前已发布数据重新验证这些URL的所有HTTP请求。 任何未连接到Dynamic Media服务URL结构且与创建公司时分配的Dynamic Media公司根ID直接匹配的URL都会导致整个请求的API出错。 CDN不支持的任何被视为无效的无效URL也会导致整个请求的API出错。

**使用频率：规则**

控制此功能使用频率的规则由Dynamic Media的CDN合作伙伴控制。 CDN保留降低这些失效的响应性的酌处权，以保持其向其用户提供的服务的最佳性能。 如果Dynamic Media收到过度使用此功能的通知，Adobe必须基于每个公司或整个服务禁用该功能。

**确认电子邮件**

Dynamic Media CDN合作伙伴的确认电子邮件最多可以发送给列表创建者或其他5个电子邮件地址。 当通知整个CDN网络电子邮件中引用的URL已被清除时，API会发送确认。 如果提供的URL数量超过Dynamic Media在单个通知中可向CDN合作伙伴提供的数量，则对`cdnCacheInvalidation`的单次调用可以发送多个电子邮件。 目前，这表示请求将超过100个URL，但可能会根据CDN合作伙伴的请求而发生更改。

**自**&#x200B;起便受支持

6.0

## 授权用户类型 {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## 参数 {#section-bd1ed2b7419945d19a2ebd5668499f72}

**输入** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>名称</b> </th> 
   <th class="entry"> <b>类型</b> </th> 
   <th class="entry"> <b>必填</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd：string</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 与要失效的URL关联的公司的句柄。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph">类型：UrlArray</span> </p> </td> 
   <td> <p> 是 </p> </td> 
   <td> <p> 从CDN缓存中失效的URL列表，最多1000个。 所有URL都必须包含要失效的Dynamic Media公司根ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出**(`cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>名称</b> </th> 
   <th class="entry"> <b>类型</b> </th> 
   <th class="entry"> <b>必填</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>引用清除请求的句柄。 </p> <p><span class="codeph"> cdnCacheInvalidation</span> API现在几乎立即使缓存失效（~5秒）。 因此，通常不再需要轮询失效状态。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>预计完成清除请求的秒数。 客户端应等待此时间，然后再轮询状态。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-f414361a58e84dfcbbac30a358d02125}

此示例请求在CDN缓存中使4个URL失效。 响应包含操作成功的摘要计数和直接从CDN提供的错误详细信息列表，以协助客户端使用此功能。

`getCdnCacheInvalidationStatus`操作。

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
