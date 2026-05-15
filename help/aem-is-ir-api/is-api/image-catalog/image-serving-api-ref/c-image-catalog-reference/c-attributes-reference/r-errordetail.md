---
description: 错误消息详细信息。 将通过HTTP返回的错误消息的详细级别指定为error.message值。
solution: Experience Manager
title: 错误详细信息
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
TQID: 'https://experienceleague.adobe.com/CZ2k-H1kZI3t3ZAtgm7qj8eo97u4NPmumdErNU--uvU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 168
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
  <td class="stentry"> <p>完整的调试信息。 在适用的情况下添加Java栈栈跟踪。 错误图像从不包含栈栈跟踪，而是在<span class="codeph"> $error.message</span>中返回级别2信息。 在向Dynamic Media技术支持报告问题时，此信息可能会很有用。 </p></td> 
 </tr> 
</table>

## 属性 {#section-e167895723ca4ad4ba283d3d7b4324de}

枚举值，必须为0、1、2或3。

## 默认 {#section-8f27098e509945a18676aca0675c8f41}

如果未指定或为空，则从`default::ErrorDetail`继承。

## 另请参阅 {#section-5451b0525ed74121950bfc34726c3970}

[attribute：：ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
