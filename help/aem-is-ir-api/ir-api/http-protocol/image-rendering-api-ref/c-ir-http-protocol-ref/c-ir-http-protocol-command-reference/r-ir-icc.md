---
title: icc
description: 输出颜色配置文件。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# icc{#icc}

输出颜色配置文件。

icc= *`profile`*[， *`renderIntent`*[，*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">配置文件</span></span> </p></td> 
  <td class="stentry"> <p>ICC颜色配置文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">渲染意图</span> </span> </p></td> 
  <td class="stentry"> <p>可感知 | 相对 | 饱和度 | 绝对 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1表示启用，0表示禁用黑场补偿。 </p></td> 
 </tr> 
</table>

*`profile`*&#x200B;指定呈现的图像与工作配置文件不同时应转换到的输出色彩空间配置文件。 *`profile`*&#x200B;必须是图像目录或默认目录的ICC配置文件映射中定义的有效`icc::Name`，或者是配置文件相对路径（通常具有[!DNL `.icc`]或[!DNL `.icm`]后缀）。

>[!NOTE]
>
>*`profile`*&#x200B;不能包含“，”字符，即使使用HTTP编码也是如此。

*`renderIntent`*&#x200B;允许覆盖默认的渲染方法。

*`blackpointComp`*&#x200B;如果输出配置文件支持此功能，则启用黑点补偿。

>[!NOTE]
>
>并非所有颜色转换都支持所有&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;选择。 通常，仅当ICC输出配置文件描述打印机或显示器等输出设备时，才会遵循这些设置。 此外，某些ICC输出配置文件不支持所有&#x200B;*`renderIntent`*&#x200B;选项。

## 属性 {#section-b4042623a8ea40248c11b2153e5906b1}

可能出现在请求中的任何位置。 如果用`fmt=`指定的图像类型与&#x200B;*`profile`*&#x200B;不匹配，则返回错误。

如果&#x200B;*`renderIntent`*&#x200B;和&#x200B;*`blackpointComp`*&#x200B;与指定的ICC配置文件不兼容，则会被忽略。

CMYK输出设备配置文件更有可能支持不同的渲染意图。

## 默认 {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

如果启用了颜色管理并且未指定`icc=`，则服务器将图像传递到与`attribute::IccProfile*`指定的图像类型匹配的输出配置文件(`fmt=`)。

如果未指定，*`renderIntent`*&#x200B;继承自`attribute::IccRenderIntent`，*`blackpointComp`*&#x200B;继承自`attribute::IccBlackPointCompensation`。

## 另请参阅 {#section-37ef83149fd74345956a98f633cc0294}

[颜色管理](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)，[属性：：IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127)，[iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)，[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)，[属性：：IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)，[属性：：IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
