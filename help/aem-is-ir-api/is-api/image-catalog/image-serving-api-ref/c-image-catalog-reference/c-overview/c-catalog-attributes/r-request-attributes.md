---
description: 目录属性文件可识别这些请求属性。
solution: Experience Manager
title: 请求属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1f2905f-f4e8-4944-8b27-469f09aa4bce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# 请求属性{#request-attributes}

目录属性文件可识别这些请求属性。

语法

<table id="simpletable_2690384A0117458DB12E4E99EFDA975A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> MaxPix</a> </span> </p></td> 
  <td class="stentry"> <p>响应图像大小限制。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-allowdirecturls.md#reference-cc649a518182497baacf9f6b19559689" type="reference" format="dita" scope="local"> AllowDirectUrls</a> </span> </p></td> 
  <td class="stentry"> <p>允许绝对URL作为图像源。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> RootUrl</a> </span> </p></td> 
  <td class="stentry"> <p>相对图像源URL的根URL。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local">请求模糊处理</a> </span> </p></td> 
  <td class="stentry"> <p>请求模糊处理模式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> RequestLock</a> </span> </p></td> 
  <td class="stentry"> <p>请求锁定模式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local">水印</a> </span> </p></td> 
  <td class="stentry"> <p>水印模板选择器。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> ErrorImage</a> </span> </p></td> 
  <td class="stentry"> <p>图像或模板错误。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561" type="reference" format="dita" scope="local"> ErrorDetail</a></span> </p></td> 
  <td class="stentry"> <p>错误消息详细信息。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-trusteddomains.md#reference-563bd5c54f914d9abcd2304ab292e12f" type="reference" format="dita" scope="local"> TrustedDomains</a> </span> </p></td> 
  <td class="stentry"> <p>允许访问SWF响应图像的Web域。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf" type="reference" format="dita" scope="local"> DefaultExpiration</a> </span> </p></td> 
  <td class="stentry"> <p>默认图像响应的客户端缓存TTL。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d" type="reference" format="dita" scope="local"> NonImgExpiration</a> </span> </p></td> 
  <td class="stentry"> <p>非图像响应的客户端缓存TTL。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318" type="reference" format="dita" scope="local">区域设置映射</a></span> </p></td> 
  <td class="stentry"> <p>ID转换映射。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e" type="reference" format="dita" scope="local"> LocaleStrMap</a> </span> </p></td> 
  <td class="stentry"> <p>字符串本地化映射。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> DefaultImageMode</a> </span> </p></td> 
  <td class="stentry"> <p>默认图像行为。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68" type="reference" format="dita" scope="local"> ClientAddressFilter</a></span> </p></td> 
  <td class="stentry"> <p>客户端IP地址过滤器。 </p></td> 
 </tr> 
</table>
