---
title: 地图
description: 图像映射数据。 提供此图层的图像映射数据。 覆盖此图层的目录映射中的所有数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 2%

---

# 地图{#map}

图像映射数据。 提供此图层的图像映射数据。 覆盖此图层的catalog：：Map中的所有数据。

`map=[ *`字符串`*]mapA=[ *`stringA`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 字符串</span></span> </p></td> 
  <td class="stentry"> <p>图层坐标中此图层的图像映射数据。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>此图层的图像映射数据（以源图像坐标表示）。 </p></td> 
 </tr> 
</table>

空字符串表示此图层不应提供图像映射。 字符串必须正确进行HTTP编码，以避免出现解析问题。

中出现的所有与号(&amp;)字符 *`string`* 必须为http编码。

同时 `mapA=` 和 `catalog::Map` 以源图像坐标指定映射数据， `map=` 假定图层坐标相对于图层矩形的左上角(在 `rotate=` 和 `extend=` 中所有规则都适用的)。

输出图像映射始终被剪切到图层矩形中。 如果 `shape` 属性被忽略或设置为 `default`，则整个图层矩形用作图像映射区域。

## 属性 {#section-a18d9ea95c71414a905a68b8839c0843}

层属性。 当应用于 `layer=comp`，则指定的映射数据将位于所有其他图像映射的后面。 已忽略，除非 `req=map`. 被效果层忽略。 `mapA=` 忽略以下情况 `map=` 也会指定。

## 默认 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 使用条件 `map=` 未指定。

## 示例 {#section-cd7691c94f984222845c86dcb0051ce8}

为简单文本图层定义矩形图像映射：

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

An `AREA` 具有（通常）默认属性的元素用于插入整个图层矩形的映射区域。

## 另请参阅 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[图像映射](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)， [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
