---
description: 图像服务器代理可用于调整日语电话的图像大小。
solution: Experience Manager
title: 图像服务器代理
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 图像服务器代理{#image-server-proxy}

图像服务器代理可用于调整日语电话的图像大小。

## URL 格式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS代理的URL格式与常规IS请求非常相似。 传递给代理的任何IS修饰符都会传递到图像服务器。 您可以在[HTTP协议参考](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)中找到有关IS修饰符的信息。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## 特定于代理的修饰符列表 {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定设备可用宽度的百分比，以用作图像宽度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 海百分比=  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定要用作图像高度的设备可用高度的百分比。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>指定设备的“内存限制嵌入式媒体”属性的百分比，以将响应大小限制为。 这将仅适用于jpg响应。 在响应大小在指定的百分比内之前，图像质量会降低。 </p></td> 
 </tr> 
</table>

## 嵌入式图像内存限制 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

如果设备对可嵌入到网页上的图像大小存在限制，则只要响应格式为jpg，图像大小就会限制为该大小。 如果设备没有任何限制，则代理将响应限制为500MB。

## 后端处理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

代理每天下载、验证和加载一次Device Atlas数据文件。 验证会提取不同设备的不同属性，并在接受新数据之前将其与预期值进行比较。
