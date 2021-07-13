---
description: 如果将jsonp指定为响应格式，则回复数据将使用JSONP（带内边距的JavaScript对象表示法）进行格式化，该格式封装在JavaScript函数调用中。
solution: Experience Manager
title: JSONP属性
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# JSONP属性{#jsonp-properties}

如果将jsonp指定为响应格式，则回复数据将使用JSONP（带内边距的JavaScript对象表示法）进行格式化，该格式封装在JavaScript函数调用中。

客户端可以指定可选的唯一请求标识符(*`reqId`*)，该标识符在响应中返回，并允许客户端区分异步接收的多个响应。 典型响应的一般结构如下：

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

`s7jsonResponse` JavaScript函数必须由客户端定义。 最简单的形式是，函数可能如下所示：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法来指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。只允许使用a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.

Dynamic Media Image Serving Viewers包包含一个实用程序，用于从Image Serving中请求和解析JSONP格式的数据。

有关JSONP格式的更多信息，请参阅[http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP)。

有关JSON格式的更多信息，请参阅[www.json.org](http://www.json.org)。

另请参阅[req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
