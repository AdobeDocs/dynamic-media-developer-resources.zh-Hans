---
title: JSONP屬性
description: 如果將jsonp指定為回應格式，則會使用JSONP （JavaScript物件標籤法加內邊距）將回覆資料格式化，並包裝在JavaScript函式呼叫中。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# JSONP屬性{#jsonp-properties}

如果將jsonp指定為回應格式，則會使用JSONP （JavaScript物件標籤法加內邊距）將回覆資料格式化，並包裝在JavaScript函式呼叫中。

使用者端可以指定選用的唯一請求識別碼( *`reqId`*)，此資訊會傳回至回應，並允許使用者端區分非同步收到的多個回應。 典型回應的一般結構如下：

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

此 `s7jsonResponse` JavaScript函式必須由使用者端定義。 函式最簡單的形式可能如下所示：

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler]`

此 `<reqHandler>` 語法是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.

Dynamic Media Image Serving Viewers套件包含從Image Serving請求及剖析JSONP格式資料的公用程式。

另請參閱 [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) 以取得有關JSONP格式的詳細資訊。

另請參閱 [www.json.org](https://www.json.org/json-en.html) 以取得有關JSON格式的詳細資訊。

另請參閱 [需要](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
