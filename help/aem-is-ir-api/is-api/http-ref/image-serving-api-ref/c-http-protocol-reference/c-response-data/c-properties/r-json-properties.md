---
description: 如果将jsonp指定为响应格式，则使用JSONP（JavaScript对象表示法，带填充）格式化回复数据，该表示法封装在JavaScript函数调用中。
seo-description: 如果将jsonp指定为响应格式，则使用JSONP（JavaScript对象表示法，带填充）格式化回复数据，该表示法封装在JavaScript函数调用中。
seo-title: JSONP属性
solution: Experience Manager
title: JSONP属性
topic: Scene7 Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JSONP属性{#jsonp-properties}

如果将jsonp指定为响应格式，则使用JSONP（JavaScript对象表示法，带填充）格式化回复数据，该表示法封装在JavaScript函数调用中。

客户端可以指定可选的唯一请求标识符( *`reqId`*)，该唯一请求标识符在响应中返回并允许客户端区分异步接收的多个响应。 典型响应具有以下一般结构：

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

JavaScript `s7jsonResponse` 函数必须由客户端定义。 在最简单的形式中，该函数可能如下：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支持JSONP响应格式的请求允许您使用参数的扩展语法指定JS回调处理函数的 `req=` 名称：

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。 仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.

Scene7图像服务查看器包包含一个实用程序，用于从图像服务请求和解析JSONP格式的数据。

有关 [JSONP格式的更多信息](http://en.wikipedia.org/wiki/JSONP) ，请参阅http://en.wikipedia.org/wiki/JSONP。

有关 [JSON格式的更多信息](http://www.json.org) ，请参阅www.json.org。

另请参阅 [请求](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
