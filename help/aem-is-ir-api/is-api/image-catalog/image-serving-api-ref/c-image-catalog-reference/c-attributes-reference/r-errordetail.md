---
description: 错误消息详细信息。 将通过HTTP返回的错误消息的详细级别指定为error.message值。
solution: Experience Manager
title: 错误详细信息
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# 错误详细信息{#errordetail}

错误消息详细信息。 将通过HTTP返回的错误消息的详细级别指定为error.message值。

允许使用以下值：

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>仅限标题。 返回错误的简短常规描述。 建议对可以公开访问的实时服务器使用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>简短消息。 保留供将来使用。 当前返回的信息与0相同。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>详细消息。 提供有关错误的用户级别详细信息。 可能包括敏感信息，如文件路径。 建议用于暂存、质量保证和应用程序开发服务器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完整的调试信息。 在适用的情况下添加Java栈栈跟踪。 错误图像从不包含栈栈跟踪，而是在中返回级别2信息 <span class="codeph"> $error.message</span>. 在向Dynamic Media技术支持报告问题时，此信息可能会很有用。 </p></td> 
 </tr> 
</table>

## 属性 {#section-e167895723ca4ad4ba283d3d7b4324de}

枚举值，必须为0、1、2或3。

## 默认 {#section-8f27098e509945a18676aca0675c8f41}

继承自 `default::ErrorDetail` 如果未指定或为空。

## 另请参阅 {#section-5451b0525ed74121950bfc34726c3970}

[attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
