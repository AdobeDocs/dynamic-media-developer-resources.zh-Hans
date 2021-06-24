---
description: 输出颜色配置文件.
solution: Experience Manager
title: icc
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 4%

---

# icc{#icc}

输出颜色配置文件.

`icc= *``*[, *``*[, *``*[, *`objecttrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 对象</span> </span> </p></td> 
  <td class="stentry"> <p>ICC颜色配置文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 持久度|相对|饱和度|绝对</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1要启用，0要禁用黑点补偿。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 抖动</span></span> </p></td> 
  <td class="stentry"> <p>1启用，0禁用抖动。 </p></td> 
 </tr> 
</table>

*`object`* 指定图像与工作配置文件不同时应转换到的输出色彩空间配置文件。*`profile`* 必须是在图像目 `icc::Name` 录或默认目录的ICC配置文件映射中定义的有效路径，或配置文件的相对路径(通常带 [!DNL .icc] 或 [!DNL .icm] 后缀)。有关其他信息，请参阅[ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

>[!NOTE]
>
>*`object`* 不能包含“，”字符，即使HTTP编码也是如此。

*`renderIntent`* 允许覆盖默认渲染意图。

*`blackpointComp`* 如果输出配置文件支持此功能，则启用黑点补偿。

>[!NOTE]
>
>并非所有颜色转换都支持所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;选项。 通常，只有在ICC输出配置文件为打印机或显示器等输出设备的特征时，才会执行这些设置。 此外，某些ICC输出配置文件不支持所有&#x200B;*`renderIntent`*&#x200B;选项。

注意

*`dither`* 启用抖动（实际上是误差扩散），这可以避免或减少色带伪影。

## 属性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

请求属性。 如果指定的图像类型与&#x200B;*`profile`*&#x200B;不匹配，则服务器将返回错误。`fmt=`

*`renderIntent`* 和 *`blackpointComp`* 如果与指定的ICC配置文件不兼容，则忽略。CMYK输出设备配置文件更可能支持不同的渲染意图。

## 默认 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果启用了色彩管理并且未指定`icc=`，则服务器将传送转换到与使用`fmt=`指定的图像类型匹配的输出配置文件(`attribute::IccProfile*`)的图像。

如果未指定，则从`attribute::IccRenderIntent`继承&#x200B;*`renderIntent`*，从`attribute::IccBlackPointCompensation`继承&#x200B;*`blackpointComp`*，从`attribute::IccDither`继承&#x200B;*`dither`*。

## 另请参阅 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[属性：:IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ,  [属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [属性：:IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [属性：:IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a),  [对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [颜色管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7),  [ICC配置文件映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
