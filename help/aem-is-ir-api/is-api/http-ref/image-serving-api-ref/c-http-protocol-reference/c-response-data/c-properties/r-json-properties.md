---
title: JSONP属性
description: 如果将jsonp指定为响应格式，则会使用JSONP（带填充的JavaScript对象表示法）对回复数据进行格式化，并封装在JavaScript函数调用中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# JSONP属性{#jsonp-properties}

如果将jsonp指定为响应格式，则会使用JSONP（带填充的JavaScript对象表示法）对回复数据进行格式化，并封装在JavaScript函数调用中。

客户端可以指定可选的唯一请求标识符( *`reqId`*)，响应中会返回并允许客户端区分异步收到的多个响应。 典型响应具有以下一般结构：

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

此 `s7jsonResponse` JavaScript函数必须由客户端定义。 函数最简单的形式可能如下所示：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支持JSONP响应格式的请求允许您使用扩展语法指定JS回调处理程序的名称 `req=` 参数：

`req=...,json [&handler = reqHandler]`

此 `<reqHandler>` 语法是JSONP响应中存在的JS处理程序的名称。 仅允许a-z、A-Z和0-9字符。 可选. 默认值为 `s7jsonResponse`.

Dynamic Media图像服务查看器包包括用于从图像服务请求和解析JSONP格式数据的实用程序。

参见 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) 有关JSONP格式的详细信息。

参见 [www.json.org](https://www.json.org/json-en.html) 有关JSON格式的详细信息。

另请参阅 [需要](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
