---
description: 静态内容类型筛选器。 为通过/is/content交付的静态内容指定过滤器字符串。
solution: Experience Manager
title: 类型
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---

# 类型{#type}

静态内容类型筛选器。 为通过/is/content交付的静态内容指定过滤器字符串。

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>键入过滤器字符串。 </p></td> 
 </tr> 
</table>

服务器将比较val与请求的静态内容项的`catalog::Type`值。 如果值匹配（区分大小写），则将项目返回给客户端，否则将返回错误。

## 属性 {#section-529b088434a44a9f86a64ef548d2925b}

仅支持通过提供的静态内容（非图像）请求。 如果`catalog::Type`为空或未定义，则忽略。

## 默认 {#section-e9e8f51d0a01452183ccb510efd87d46}

如果未指定`type=`或为空，则不应用类型匹配。

## 另请参阅 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[提供静态（非图像）内容](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [目录：::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
