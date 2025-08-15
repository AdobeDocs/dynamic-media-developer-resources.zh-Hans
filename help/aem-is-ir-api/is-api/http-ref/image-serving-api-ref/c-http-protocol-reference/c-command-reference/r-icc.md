---
title: icc
description: 输出颜色配置文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# icc{#icc}

输出颜色配置文件。

`icc= *`对象`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">对象</span> </span> </p></td> 
  <td class="stentry"> <p>ICC颜色配置文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">可感知|相对|饱和度|绝对</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1表示启用，0表示禁用黑场补偿。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">仿色</span></span> </p></td> 
  <td class="stentry"> <p>1表示启用，0表示禁用仿色。 </p></td> 
 </tr> 
</table>

如果值&#x200B;*`object`*&#x200B;与工作配置文件不同，则指定图像应转换到的输出色彩空间配置文件。 值&#x200B;*`profile`*&#x200B;必须是图像目录或默认目录的ICC配置文件映射中定义的有效`icc::Name`，或者是配置文件相对路径（通常具有[!DNL .icc]或[!DNL .icm]后缀）。 请参阅[*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)以了解更多信息。

>[!NOTE]
>
>值&#x200B;*`object`*&#x200B;不能包含“，”字符，即使使用HTTP编码也是如此。

值&#x200B;*`renderIntent`*&#x200B;允许覆盖默认的渲染方法。

如果输出配置文件支持此功能，则值&#x200B;*`blackpointComp`*&#x200B;将启用黑点补偿。

>[!NOTE]
>
>并非所有颜色转换都支持所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;选择。 通常，仅当ICC输出配置文件描述打印机或显示器等输出设备时，才会遵循这些设置。 此外，某些ICC输出配置文件不支持所有&#x200B;*`renderIntent`*&#x200B;选项。

注意

修饰符&#x200B;*`dither`*&#x200B;启用仿色（实际上是误差扩散），可避免或减少色带伪像。

## 属性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

请求属性。 如果用`fmt=`指定的映像类型与&#x200B;*`profile`*&#x200B;不匹配，则服务器返回错误。

如果与指定的ICC配置文件不兼容，则忽略修饰符&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*。 CMYK输出设备配置文件更有可能支持不同的渲染意图。

## 默认 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果启用了颜色管理并且未指定`icc=`，则服务器将图像传递到与`attribute::IccProfile*`指定的图像类型匹配的输出配置文件(`fmt=`)。

如果未指定，*`renderIntent`*&#x200B;继承自`attribute::IccRenderIntent`，*`blackpointComp`*&#x200B;继承自`attribute::IccBlackPointCompensation`，*`dither`*&#x200B;继承自`attribute::IccDither`。

## 另请参阅 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute：：IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ，[attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，[attribute：：IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)，[attribute：：IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)，[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)，[对象](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)，[颜色管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)，[ICC配置文件映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)，[iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
