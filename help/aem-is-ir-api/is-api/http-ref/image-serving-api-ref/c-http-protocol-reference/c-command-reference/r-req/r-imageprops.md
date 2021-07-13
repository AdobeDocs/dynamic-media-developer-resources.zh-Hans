---
description: 源图像属性。 返回在URL路径中指定的图像文件或目录条目的选定属性。
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 10%

---

# imageprops{#imageprops}

源图像属性。 返回在URL路径中指定的图像文件或目录条目的选定属性。

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

HTTP 响应是可缓存的，且 TTL 基于 `attribute::NonImgExpiration`.

请求字符串中的其他命令将被忽略。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法来指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。只允许使用a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.

返回以下属性：

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> 属性</b> </td> 
   <td> <b> 类型</b> </td> 
   <td> <b> 说明</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int，int </p> </td> 
   <td> <p> <span class="codeph"> 目录：:</span> 锚点或默认锚点 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> 双 </p> </td> 
   <td> <p> <span class="codeph"> 目录：:</span> 过期或默认存留时间 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>全分辨率图像高度（以像素为单位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 与此图像关联的配置文件的名称/描述 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 图像. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 如果关联的配置文件嵌入到图像中，则为1 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> 布尔 </p> </td> 
   <td> <p> 1(如果图像包含Photoshop路径数据) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 图像. embeddedXmpData</span> </p> </td> 
   <td> <p> 布尔 </p> </td> 
   <td> <p> 1(如果图像包含XMP数据) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> 枚举 </p> </td> 
   <td> <p> 0表示无蒙版，1表示预乘α,2表示非预乘α,3表示单独的蒙版图像 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 目录：:</span> 如果不是目录条目，则修改器为空 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 图像. photoshopPathNames</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 与此图像关联的所有Photoshop路径的名称列表（以逗号分隔） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 图像类型，可以是“CMYK”、“RGB”或“BW”（对于灰度图像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> <span class="codeph"> 属性：:</span> 如果不是目录条目，则为空 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> 默认打印分辨率（以像素/英寸为单位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> 目录：:</span> 分辨率或默认对象分辨率 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p>修改日期/时间（从<span class="codeph">目录：:TimeStamp</span>或图像文件） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> 真实 </p> </td> 
   <td> <p> <span class="codeph"> 目录：:</span> 缩览图重置默认缩略图分辨率 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> 枚举 </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> ThumbType或默认缩略图类型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 全分辨率图像宽度（以像素为单位） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> 字串 </p> </td> 
   <td> <p> 将路径中指定的<span class="varname">对象</span>解析到的目录ID（请参阅<a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local">对象ID转换</a>）。 </p> </td> 
  </tr> 
 </tbody> 
</table>
