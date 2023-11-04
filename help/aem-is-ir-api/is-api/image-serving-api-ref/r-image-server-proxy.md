---
description: 图像服务器代理可用于调整日语手机的图像大小。
solution: Experience Manager
title: 图像服务器代理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# 图像服务器代理{#image-server-proxy}

图像服务器代理可用于调整日语手机的图像大小。

## URL 格式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS代理的URL格式与常规IS请求非常相似。 传递给代理的任何IS修饰符都会传递到图像服务器。 有关IS修饰符的信息，请参阅 [HTTP协议参考](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## 特定于代理的修饰符列表 {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要用作图像宽度的设备可用宽度的百分比。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 海百分比= &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要用作图像高度的设备可用高度的百分比。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要将响应大小限制到的设备内存限制嵌入式媒体属性的百分比。 这仅适用于jpg响应。 图像质量会降低，直到响应大小在指定的百分比内。 </p></td> 
 </tr> 
</table>

## 嵌入式映像内存限制 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

如果设备对可以嵌入到网页上的图像大小有限制，则只要响应格式为jpg，图像大小就限制为该尺寸。 如果设备没有任何限制，代理将响应限制为500MB。

## 后端处理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

代理每天下载、验证和加载Device Atlas数据文件一次。 验证会为不同的设备提取不同的属性，并在接受新数据之前将其与预期值进行比较。
