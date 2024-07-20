---
title: 图像集
description: 图像集。 指定生成req=set响应时使用的图像集值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 4%

---

# 图像集{#imageset}

图像集。 指定生成req=set响应时使用的图像集值。

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span></span> </p> </td> 
  <td class="stentry"> <p>图像集字符串。 </p></td> 
 </tr> 
</table>

要对值进行转义并确保包含的任何修饰符都不会解释为URL查询字符串的一部分，应将整个值括在大括号中。 如果在网络路径中指定了目录记录，则此修饰符值将覆盖主记录中的`catalog::ImageSet`。 有关有效图像集语法的说明，请参阅`catalog::ImageSet`文档。

## 属性 {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

请求属性。 可选。 覆盖主记录中的`catalog::ImageSet`。

## 默认 {#section-e8622ff40408450fb79d028f8d37fa6b}

无。

## 示例 {#section-68513d3c601f477399602a0741dab390}

指定用于`req=set`请求的图像集：

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## 另请参阅 {#section-7e0320b2e09d475897082711a8f023a9}

[catalog：：ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ， [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)， [媒体集请求](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
