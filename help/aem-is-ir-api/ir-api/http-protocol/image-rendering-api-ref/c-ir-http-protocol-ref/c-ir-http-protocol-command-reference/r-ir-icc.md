---
description: 输出颜色用户档案。
seo-description: 输出颜色用户档案。
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

输出颜色用户档案。

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 用户档案</span></span> </p></td> 
  <td class="stentry"> <p>ICC颜色用户档案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span></span> </p></td> 
  <td class="stentry"> <p>知觉|相对|饱和度|绝对 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1表示启用，0表示禁用黑点补偿。 </p></td> 
 </tr> 
</table>

*`profile`* 指定渲染后的图像应转换到的输出色彩空间用户档案(如果它与工作用户档案不同)。 *`profile`* 必须是图像目录或 `icc::Name` 默认目录的ICC用户档案映射中定义的有效路径，或用户档案文件的相对路径(通常带有或 [!DNL .icc]后 [!DNL .icm] 缀)。

>[!NOTE]
>
>*`profile`* 不能包括&#39;,&#39;字符，即使HTTP编码也是如此。

*`renderIntent`* 允许覆盖默认渲染方法。

*`blackpointComp`* 如果输出用户档案支持此功能，则启用黑点补偿。

>[!NOTE]
>
>并非所有颜色转换都支持所有 *`renderIntent`* 选项和 *`blackpointComp`* 选项。 通常，仅当ICC输出用户档案特征化输出设备（如打印机或显示器）时，才执行这些设置。 此外，某些ICC输出用户档案不支持所有选 *`renderIntent`* 择。

## 属性 {#section-b4042623a8ea40248c11b2153e5906b1}

可能发生在请求内的任何位置。 如果指定的图像类型与不匹配，则 `fmt=` 会返回错误 *`profile`*。

*`renderIntent`* 如果 *`blackpointComp`* 与指定的ICC用户档案不兼容，则忽略此参数。

CMYK输出设备用户档案更有可能支持不同的渲染方法。

## 默认 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

如果启用颜色管理且 `icc=` 未指定，则服务器将传送转换为与指定的图像类型匹配的输出用户档案( `attribute::IccProfile*`)的图像 `fmt=`。

如果未指定， *`renderIntent`* 则从中继 `attribute::IccRenderIntent`承， *`blackpointComp`* 并从中继承 `attribute::IccBlackPointCompensation`。

## 另请参阅 {#section-37ef83149fd74345956a98f633cc0294}

[颜色管理](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)，属 [性：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)= [,](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)[](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)[Attribute:IccRenderIntentFmt属性，属性：IccProfile*, iccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
