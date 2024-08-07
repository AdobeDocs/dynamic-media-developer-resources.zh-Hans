---
description: 响应数据属性。 评估当前请求，就像它是一个图像请求(req=img)，但服务器不返回图像，而是返回回复图像的选定属性。
solution: Experience Manager
title: prop
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 5%

---

# prop{#props}

响应数据属性。 评估当前请求，就像它是一个图像请求(req=img)，但服务器不返回图像，而是返回回复图像的选定属性。

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId </span> </span> </p> </td> 
  <td class="stentry"> <p>唯一请求标识符。 </p> </td> 
 </tr> 
</table>

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选。 默认值为`s7jsonResponse`。

有关回复语法和响应MIME类型的说明，请参阅[属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9)。 可使用基于`attribute::NonImgExpiration`的TTL来缓存HTTP响应。

将为/is/image请求返回以下属性：

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b>属性</b> </td> 
   <td> <b>类型</b> </td> 
   <td> <b>描述</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 十六进制 </p> </td> 
   <td> <p> 背景颜色（请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 回复图像高度（以像素为单位） </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果ICC配置文件嵌入到回复图像中，则为True。 （请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 与回复图像关联的配置文件的名称/描述。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 回复大小，以像素为单位，不包括HTTP标头；如果服务器之前未缓存回复图像数据，则为0。 （请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 枚举 </p> </td> 
   <td> <p> 如果回复图像包含Alpha通道，则为1，否则为0。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回复图像类型，可以是<span class="codeph"> CMYK </span>、<span class="codeph">RGB</span>或<span class="codeph"> BW </span>（用于灰度图像）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果响应图像嵌入了任何路径，则为1，否则为0。 （请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local">路径嵌入= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> 打印分辨率(dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> JPEG质量。 （请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 回复图像的MIME类型。 （请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 回复图像宽度（像素）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果响应图像嵌入了xmp数据，则为1，否则为0。 （请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 图像版本标识符。 （请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>。） </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 元数据版本标识符。 （请参阅<span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>。） </p> </td> 
  </tr> 
 </tbody> 
</table>

为`/is/content`请求返回以下属性：

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b>属性</b> </td> 
   <td> <b>类型</b> </td> 
   <td> <b>描述</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">路径</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p>部分解析的文件路径。 （请参阅<span class="codeph">静态：：路径</span>。） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">长度</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> 对象文件大小（以字节为单位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">过期</span> </p> </td> 
   <td> <p> 双 </p> </td> 
   <td> <p> <span class="codeph">静态：：过期</span>或默认生存时间 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified </span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 修改日期/时间（来自<span class="codeph"> static：：TimeStamp </span>或对象文件） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">用户类型</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph">静态：：UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
