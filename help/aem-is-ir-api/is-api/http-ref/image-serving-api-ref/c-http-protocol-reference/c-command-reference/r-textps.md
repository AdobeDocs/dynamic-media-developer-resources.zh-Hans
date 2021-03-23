---
description: 图层文本(Adobe Photoshop兼容)。 指定文本图层的文本正文。
seo-description: 图层文本(Adobe Photoshop兼容)。 指定文本图层的文本正文。
seo-title: textPs
solution: Experience Manager
title: textPs
uuid: 45e587b6-8dc8-408c-ade6-d70025fd1117
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 4%

---


# textPs{#textps}

图层文本(Adobe Photoshop兼容)。 指定文本图层的文本正文。

`textPs= *`字串`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 字符串</span> </span> </p> </td> 
  <td class="stentry"> <p>富文本格式(RTF)字符串。 </p></td> 
 </tr> 
</table>

所有字体、字体颜色和段落格式控制都可使用RTF命令实现。

请参阅[文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)。

`textPs=` 支持扩展功能，如对齐、将文本流入用和/或定义的非矩形 `textFlowPath=` 区域以 `textFlowXPath=`及沿用定义的任意路径呈现文本 `textPath=`。

## 属性 {#section-a289dc26b6534b41998b1e241d5f2f92}

图层属性。 适用于`layer=comp`时的`layer=0`。 与同一层中的`src=`和`text=`互斥。 最后一次出现`text=`、`textPs=`和`src=`的情况将占上风，并确定这是图像还是文本图层。 被效果图层忽略。

## 默认 {#section-11c2ae2c96d64a0a9c207252df663e4d}

无。

## 另请参阅 {#section-5c2b25767d2b47b5be817271ab12e13c}

[文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), textAttr= [, textFlowText](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) [=, TextFlowFlowXPXP=, textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
