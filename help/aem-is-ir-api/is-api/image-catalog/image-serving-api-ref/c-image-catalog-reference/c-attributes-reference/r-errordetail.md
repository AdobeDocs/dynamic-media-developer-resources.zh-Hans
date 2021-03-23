---
description: 错误消息详细信息。 指定通过HTTP返回的错误消息的详细信息级别为error.message值。
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 4%

---


# ErrorDetail{#errordetail}

错误消息详细信息。 指定通过HTTP返回的错误消息的详细信息级别为error.message值。

允许使用以下值：

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>仅限标题。 返回错误的简短常规描述。 建议用于可公开访问的实时服务器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>简短消息。 保留供将来使用。 当前返回与0相同的信息。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>详细消息。 提供有关错误的用户级详细信息。 可能包括敏感信息，如文件路径。 建议用于暂存、质量保证和应用程序开发服务器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完整调试信息。 添加Java堆栈跟踪（如果适用）。 错误图像从不包含堆栈跟踪，而是返回<span class="codeph"> $error.message</span>中的2级信息。 当将问题报告到Dynamic Media技术支持时，此信息可能很有用。 </p></td> 
 </tr> 
</table>

## 属性 {#section-e167895723ca4ad4ba283d3d7b4324de}

枚举值必须为0、1、2或3。

## 默认 {#section-8f27098e509945a18676aca0675c8f41}

如果未指定或为空，则从`default::ErrorDetail`继承。

## 另请参阅 {#section-5451b0525ed74121950bfc34726c3970}

[属性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
