---
description: 如果将jsonp指定为响应格式，则使用JSONP（带边距的JavaScript对象表示法）格式化回复数据，它打包在JavaScript函数调用中。
seo-description: 如果将jsonp指定为响应格式，则使用JSONP（带边距的JavaScript对象表示法）格式化回复数据，它打包在JavaScript函数调用中。
seo-title: JSONP属性
solution: Experience Manager
title: JSONP属性
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---


# JSONP属性{#jsonp-properties}

如果将jsonp指定为响应格式，则使用JSONP（带边距的JavaScript对象表示法）格式化回复数据，它打包在JavaScript函数调用中。

客户端可以指定可选的唯一请求标识符(*`reqId`*)，该标识符在响应中返回并允许客户端区分异步接收的多个响应。 典型响应具有以下一般结构：

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

`s7jsonResponse` JavaScript函数必须由客户端定义。 在最简单的形式中，该函数可能如下：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.

Dynamic Media图像服务查看器包包含一个实用程序，用于从图像服务请求和分析JSONP格式的数据。

有关JSONP格式的详细信息，请参阅[http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP)。

有关JSON格式的详细信息，请参阅[www.json.org](http://www.json.org)。

另请参阅[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
