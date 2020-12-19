---
description: 图像映射数据。 为此图层提供图像映射数据。 覆盖此图层的目录映射中的所有数据。
seo-description: 图像映射数据。 为此图层提供图像映射数据。 覆盖此图层的目录映射中的所有数据。
seo-title: 地图
solution: Experience Manager
title: 地图
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c1c3323-21ab-4820-bf4e-761b82ada1ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

---


# 地图{#map}

图像映射数据。 为此图层提供图像映射数据。 覆盖目录中的所有数据：：此图层的映射。

`map=[ *`字符串`*]mapA=[ *`A`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 字符串</span></span> </p></td> 
  <td class="stentry"> <p>在图层坐标中此图层的图像映射数据。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>在源图像坐标中此层的图像映射数据。 </p></td> 
 </tr> 
</table>

空字符串表示此层不应提供图像映射。 字符串必须正确进行HTTP编码，以避免出现解析问题。

*`string`*&#x200B;中出现的所有&amp;符字符必须采用http编码。

当`mapA=`和`catalog::Map`在源图像坐标中指定地图数据时，`map=`假定图层坐标相对于图层矩形的左上角（在应用`rotate=`和`extend=`之后）。

输出图像映射始终被剪切到图层矩形。 如果忽略`shape`属性或将其设置为`default`，则整个图层矩形将用作图像映射区域。

## 属性 {#section-a18d9ea95c71414a905a68b8839c0843}

图层属性。 当应用到`layer=comp`时，指定的映射数据将分层到所有其他图像映射之后。 除非`req=map`，否则忽略。 被效果图层忽略。 `mapA=` 如果也指 `map=` 定了，则忽略。

## 默认 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map` 在未指定 `map=` 时使用。

## 示例 {#section-cd7691c94f984222845c86dcb0051ce8}

为简单文本图层定义矩形图像映射：

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

具有（大部分）默认属性的`AREA`元素用于插入整个层矩形的映射区域。

## 另请参阅 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[图像映射](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
