---
title: 类型
description: 静态内容类型过滤器。 为通过/is/content提供的静态内容指定过滤器字符串。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# 类型{#type}

静态内容类型过滤器。 为通过/is/content提供的静态内容指定过滤器字符串。

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>键入筛选字符串。 </p></td> 
 </tr> 
</table>

服务器将`val`与所请求的静态内容项的`catalog::Type`的值进行比较。 如果值匹配（区分大小写），则会将该项目返回到客户端，否则会返回错误。

## 属性 {#section-529b088434a44a9f86a64ef548d2925b}

仅支持通过提供的静态内容（非图像）请求。 如果`catalog::Type`为空或未定义，则忽略。

## 默认 {#section-e9e8f51d0a01452183ccb510efd87d46}

如果未指定`type=`或为空，则不会应用任何类型匹配。

## 另请参阅 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[提供静态（非图像）内容](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da)，[目录：：：UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
