---
description: 选择“效果图层”。 选择效果层并开始请求字符串中与当前层关联的新层段。
seo-description: 选择“效果图层”。 选择效果层并开始请求字符串中与当前层关联的新层段。
seo-title: 效果
solution: Experience Manager
title: 效果
topic: Scene7 Image Serving - Image Rendering API
uuid: 622dc7ca-55b8-4a82-b9a7-65588aee87d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# effect{#effect}

选择“效果图层”。 选择效果层并开始请求字符串中与当前层关联的新层段。

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>效果图层编号（int不等于0）。 </p></td> 
 </tr> 
</table>

新段内的所有命令将应用到指定的效果图层。 效果层段由下一个或命 `layer=` 令或 `effect=` 请求的结束终止。

*`n`* 对于外层效果（即，父层后的效果），必须小于0；对于内层效果（即，父层内的效果），必须大于0。 效果图层编号不必是连续的。

如果同一父图层有多个效果图层，效果图层编号将指定z顺序。 编号较高的图层放置在编号较低的图层上方。

效果层可附着到 `layer=comp`。

## 属性 {#section-e11f795deff345779ce280a82cf221ca}

效果图层命令。 *`n`* 不得为0。

## 默认 {#section-84bbe1cfe7a94040827c994323ac59d4}

无。

## 示例 {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## 另请参阅 {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
