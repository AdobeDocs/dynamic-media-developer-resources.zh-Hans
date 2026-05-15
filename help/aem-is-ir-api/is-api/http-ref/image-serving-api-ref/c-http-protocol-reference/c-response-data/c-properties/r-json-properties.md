---
title: JSONP属性
description: 如果将jsonp指定为响应格式，则会使用JSONP（带填充的JavaScript对象表示法）对回复数据进行格式化，并在JavaScript函数调用中封装。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
TQID: 'https://experienceleague.adobe.com/pMirwhZ5n0mVuK2If4kJz3XDQZPDhORJCZBLsDf2C8I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# JSONP属性{#jsonp-properties}

如果将jsonp指定为响应格式，则会使用JSONP（带填充的JavaScript对象表示法）对回复数据进行格式化，并在JavaScript函数调用中封装。

客户端可以指定可选的唯一请求标识符(*`reqId`*)，该标识符在响应中返回，并允许客户端区分异步接收的多个响应。 典型响应具有以下一般结构：

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

`s7jsonResponse` JavaScript函数必须由客户端定义。 函数最简单的形式可能如下所示：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler]`

`<reqHandler>`语法是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选. 默认值为`s7jsonResponse`。

Dynamic Media图像服务查看器包包括用于从图像服务请求和解析JSONP格式数据的实用程序。

有关JSONP格式的详细信息，请参阅[https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP)。

有关JSON格式的详细信息，请参阅[www.json.org](https://www.json.org/json-en.html)。

另请参阅[请求](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)。
