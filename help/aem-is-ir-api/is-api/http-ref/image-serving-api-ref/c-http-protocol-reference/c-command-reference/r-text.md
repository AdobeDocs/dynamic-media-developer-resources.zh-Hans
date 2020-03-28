---
description: 图层文本。 指定文本图层的文本和格式化内容。
seo-description: 图层文本。 指定文本图层的文本和格式化内容。
seo-title: 文字
solution: Experience Manager
title: 文字
topic: Scene7 Image Serving - Image Rendering API
uuid: 5b4f9282-83a3-488d-b5d2-deb2c92de564
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 文字{#text}

图层文本。 指定文本图层的文本和格式化内容。

` text= *`字串`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 字串 </span> </p> </td> 
  <td class="stentry"> <p>富文本格式(RTF)字符串或纯文本字符串。 </p> </td> 
 </tr> 
</table>

所有字体、字体颜色和段落格式控制都使用RTF命令实现。 有关其 [他信息，请参阅](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) “文本格式”。

`text=` 支持自动缩放文本以填充使用指定的图层矩形 `size=`。

请参 [阅textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)。

`text=` 支持自动调整文本图层的大小以适合渲染的文本(当 `size=` 未指定或仅指定宽度时)。 请注意，在这种情况下，只能应用RTF对齐 `\ql`命令 `\qr`和 `\qc` 其中一个；否则将返回错误。

## 属性 {#section-8c0f020094a44c6b858454ef91ab4edf}

图层属性。 适用于 `layer=0` if `layer=comp`。 与同一层 `src=` 相互 `textPs=` 排斥，最后一次出现 `text=`、 `textPs=`和时 `src=` 间优先，并确定这是图像还是文本图层。 被效果图层忽略。

## 默认 {#section-58958671e0ad479e8d5f6c1d41d7dc74}

无。

## 示例 {#section-d011f765ec5c418d814a821019b0eef0}

请参阅文本格式 [和模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) A [示例](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) 中的 [示例](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另请参阅 {#section-207b779ab67342a5acd343e6bcc749c4}

[文本格式](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c)化文本 [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87)src= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)Attr= [，文本定位](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)[,Ps=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
