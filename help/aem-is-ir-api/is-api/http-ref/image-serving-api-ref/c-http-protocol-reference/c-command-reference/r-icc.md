---
description: 输出颜色配置文件.
seo-description: 输出颜色配置文件.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

输出颜色配置文件.

`icc= *`对`*[, *``*[, *``*[, *`象IntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 对 <span class="varname"> 象</span></span> </p></td> 
  <td class="stentry"> <p>ICC颜色用户档案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> renderIntent <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 可感知|相对|饱和度|绝对</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1表示启用，0表示禁用黑点补偿。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 抖动</span></span> </p></td> 
  <td class="stentry"> <p>1表示启用，0表示禁用仿色。 </p></td> 
 </tr> 
</table>

*`object`* 指定图像与工作用户档案不同时应转换到的输出色彩空间用户档案。 *`profile`* 必须是图像目录或 `icc::Name`[!DNL .icc][!DNL .icm] 默认目录的ICC用户档案映射中定义的有效路径，或用户档案文件的相对路径（通常带有或后缀）。 请参 [ 阅，了 *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)解更多信息。

>[!NOTE]
>
>*`object`* 不能包括&#39;,&#39;字符，即使HTTP编码也是如此。

*`renderIntent`* 允许覆盖默认渲染方法。

*`blackpointComp`* 如果输出用户档案支持此功能，则启用黑点补偿。

>[!NOTE]
>
>并非所有颜色转换都支持所有 *`renderIntent`* 选项和 *`blackpointComp`* 选项。 通常，仅当ICC输出用户档案特征化输出设备（如打印机或显示器）时，才执行这些设置。 此外，某些ICC输出用户档案不支持所有选 *`renderIntent`* 择。

注意

*`dither`* 启用仿色（实际上是误差扩散），这可以避免或减少色带伪影。

## 属性 {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

请求属性。 如果指定的图像类型与不匹配，则服 `fmt=` 务器将返回错误 *`profile`*。

*`renderIntent`* 如果 *`blackpointComp`* 与指定的ICC用户档案不兼容，则忽略此参数。 CMYK输出设备用户档案更有可能支持不同的渲染方法。

## 默认 {#section-0b9fe2eb428447df8ae9948f11ab5aae}

如果启用颜色管理且 `icc=` 未指定，则服务器将传送转换为与指定的图像类型匹配的输出用户档案( `attribute::IccProfile*`)的图像 `fmt=`。

如果未指定， *`renderIntent`* 则从中继 `attribute::IccRenderIntent`承、 *`blackpointComp`* 从中继承 `attribute::IccBlackPointCompensation`，并 *`dither`* 从中继承 `attribute::IccDither`。

## 另请参阅 {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[属性：::Profile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ，属性：:RenderPointPointPointP [，属性：IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[属性：IccDitherFmt,Fmt,ObjectObject,CompasingColorManagement Color,ICCiccReferenceInte,BentIntBeIcBe,BeInt,icIntIncBe.intInt.IcInt.=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
