---
description: 图像服务器代理可用于调整日文电话的图像大小。
seo-description: 图像服务器代理可用于调整日文电话的图像大小。
seo-title: 图像服务器代理
solution: Experience Manager
title: 图像服务器代理
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# 图像服务器代理{#image-server-proxy}

图像服务器代理可用于调整日文电话的图像大小。

## URL 格式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS代理的url格式与常规IS请求非常相似。 传递给代理的任何IS修饰符都会传递到图像服务器。 您可以在[HTTP协议参考](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)中找到IS修饰符的相关信息。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## 特定于代理的修饰符列表{#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定设备可用宽度的百分比，以用作图像宽度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 海百分比=  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定设备可用高度的百分比，以用作图像高度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定设备的“内存限制嵌入式媒体”属性的百分比，以将响应大小限制为。 这将仅适用于jpg响应。 在响应大小在指定百分比之内之前，图像的质量会降低。 </p></td> 
 </tr> 
</table>

## 嵌入的图像内存限制{#section-52f7c69ed8a341ceabf92ceee19b0f36}

如果设备对可嵌入网页的图像大小有限制，只要响应格式为jpg，图像大小就限制为该大小。 如果设备没有任何限制，则代理将响应限制为500MB。

## 后端处理{#section-bdf7c294b6824de9969c97fc1f8aa6d3}

代理每天下载、验证和加载Device Atlas数据文件一次。 在接受新数据之前，验证会提取不同设备的不同属性并将它们与预期值进行比较。
