---
description: 静态内容类型过滤器。 为通过/is/content传送的静态内容指定过滤器字符串。
seo-description: 静态内容类型过滤器。 为通过/is/content传送的静态内容指定过滤器字符串。
seo-title: 类型
solution: Experience Manager
title: 类型
topic: Scene7 Image Serving - Image Rendering API
uuid: 44906190-516c-481c-9714-bb19d77af33c
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# 类型{#type}

静态内容类型过滤器。 为通过/is/content传送的静态内容指定过滤器字符串。

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>键入过滤器字符串。 </p></td> 
 </tr> 
</table>

服务器将比较val与所请求的静 `catalog::Type` 态内容项的值。 如果值匹配（区分大小写），则项将返回给客户端，否则将返回错误。

## 属性 {#section-529b088434a44a9f86a64ef548d2925b}

仅支持通过提供的静态内容（非图像）请求。 如果为空 `catalog::Type` 或未定义，则忽略。

## 默认 {#section-e9e8f51d0a01452183ccb510efd87d46}

如果未指定或为空， `type=` 则不应用类型匹配。

## 另请参阅 {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[服务静态（非图像）内容](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [目录：::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
