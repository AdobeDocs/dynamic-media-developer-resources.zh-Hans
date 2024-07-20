---
title: 错误详细信息
description: 错误消息详细信息。 将通过HTTP返回的错误消息的详细级别指定为error.message值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 4%

---

# 错误详细信息{#errordetail}

错误消息详细信息。 将通过HTTP返回的错误消息的详细级别指定为error.message值。

## 标题 {#section-c10d75d72ee24d16a67cc8d927f1deba}

允许使用以下值：

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>仅限标题。 返回错误的简短常规描述。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>简短消息。 保留供将来使用。 当前返回的信息与0相同。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>详细消息。 提供有关错误的用户级别详细信息。 可能包括敏感信息，如文件路径。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>完整的调试信息。 在适用的情况下添加Java™栈栈跟踪。 错误图像从不包含栈栈跟踪，而是在<span class="codeph"> $error.message</span>中返回级别2信息。 </p></td> 
 </tr> 
</table>

* 对于可以公开访问的实时服务器，建议使用0级。
* 建议将第2级用于暂存、质量保证和应用程序开发服务器。
* 向Dynamic Media技术支持报告问题时，级别3信息可能会很有用。

## 属性 {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

枚举值，必须为0、1、2或3。

## 默认 {#section-5e78d550050840cc9a1de811c581b94f}

如果未指定或为空，则从`default::ErrorDetail`继承。

## 另请参阅 {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute：：ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
