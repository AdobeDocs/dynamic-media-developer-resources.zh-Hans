---
description: 输出颜色配置文件.
seo-description: 输出颜色配置文件.
seo-title: ic
solution: Experience Manager
title: ic
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---


# icc{#icc}

输出颜色配置文件.

`icc= *``*[, *``*[, *``*[, *`objecttrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 对象</span> </span> </p></td> 
  <td class="stentry"> <p>ICC颜色用户档案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 可感知|relative|saturation|absolute</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1表示启用，0表示禁用黑点补偿。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 抖动</span></span> </p></td> 
  <td class="stentry"> <p>启用1，禁用抖动。 </p></td> 
 </tr> 
</table>

*`object`* 指定图像与工作用户档案不同时应转换到的输出色彩空间用户档案。*`profile`* 必须是图像目 `icc::Name` 录或默认目录的ICC用户档案映射中定义的有效路径，或是用户档案文件(通常带有或 [!DNL .icc] 后缀 [!DNL .icm] 的路径)。有关其他信息，请参见[ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)。

>[!NOTE]
>
>*`object`* 不能包含“，”字符，即使是HTTP编码的字符。

*`renderIntent`* 允许覆盖默认渲染方法。

*`blackpointComp`* 如果输出用户档案支持此功能，则启用黑点补偿。

>[!NOTE]
>
>并非所有颜色转换都支持所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;选项。 通常，仅当ICC输出用户档案特征化输出设备（如打印机或显示器）时才执行这些设置。 此外，某些ICC输出用户档案不支持所有&#x200B;*`renderIntent`*&#x200B;选项。

注意

*`dither`* 启用仿色（实际上是误差扩散），这可避免或减少色带伪影。

## 属性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

请求属性。 如果使用与&#x200B;*`profile`*&#x200B;不匹配的`fmt=`指定图像类型，则服务器将返回错误。

*`renderIntent`* 如果 *`blackpointComp`* 与指定的ICC用户档案不兼容，则忽略。CMYK输出设备用户档案更可能支持不同的渲染方法。

## 默认 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果启用了色彩管理并且未指定`icc=`，则服务器将传送转换为与使用`fmt=`指定的图像类型匹配的输出用户档案(`attribute::IccProfile*`)的图像。

如果未指定，则从`attribute::IccRenderIntent`继承&#x200B;*`renderIntent`*，从`attribute::IccBlackPointCompensation`继承&#x200B;*`blackpointComp`*，从`attribute::IccDither`继承&#x200B;*`dither`*。

## 另请参阅 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[属性：:IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) *，属 [性：:IccBlackPointPint](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)，属 [性：:IccBlackBlackPointProint](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)，属性：IccDither [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) [,FmtObjectObjectOmbjectMapIng，IC.=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
