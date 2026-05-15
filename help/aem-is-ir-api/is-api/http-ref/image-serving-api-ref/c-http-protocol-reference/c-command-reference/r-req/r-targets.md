---
description: 缩放图像目录中的目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
TQID: 'https://experienceleague.adobe.com/3JPTLaprpB2W2G-ua8CxAOShG3C7kinQB5u12Dv29bQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 188
ht-degree: 1%

---

# 目標{#targets}

缩放图像目录中的目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。

`req=targets[,text|{xml[, *`编码`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">编码</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

返回`catalog::Targets`的内容。 当请求“文本”格式时，`catalog::Targets`中`??`的所有实例都替换为行终止符，并在结尾处附加一个单行终止符(`CR/LF`)。 如果URL路径未解析为有效的目录条目，则响应仅由单行终止符组成。 在请求“xml”或“json”格式时应用相应的格式。

请求字符串中的其他命令将被忽略。

可使用基于`catalog::Expiration`的TTL来缓存HTTP响应。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选. 默认值为`s7jsonResponse`。
