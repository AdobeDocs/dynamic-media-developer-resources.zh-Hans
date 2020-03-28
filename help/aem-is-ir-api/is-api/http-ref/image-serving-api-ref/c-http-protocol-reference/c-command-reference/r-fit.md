---
description: 响应图像适合模式。 指定如何计算缩放因子，当用wid=和hei=指定响应大小且scl=不存在时，缩放因子用于将合成图像缩放为响应图像。
seo-description: 响应图像适合模式。 指定如何计算缩放因子，当用wid=和hei=指定响应大小且scl=不存在时，缩放因子用于将合成图像缩放为响应图像。
seo-title: 适合
solution: Experience Manager
title: 适合
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 适合{#fit}

响应图像适合模式。 指定如何计算缩放因子，当用wid=和hei=指定响应大小且scl=不存在时，缩放因子用于将合成图像缩放为响应图像。

` fit= *`Modesupcale`*, *``*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 模式 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 适合|约束|裁剪|绕排|伸缩|适合|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 高档 </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

在下面的模式选项描述中，假定合成图像宽度与响应图像宽度的比值， *`xScale`**`yScale`* 是合成图像高度与响应图像高度的比值。

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 参数 </th> 
   <th colname="col2" class="entry"> 定义 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 适合 </span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像，使其适合使用wid=和hei= <span class="codeph"> 分配的空间 </span> , <span class="codeph"> 并且最小的空 </span>格和不裁切。 响应图像的大小将与wid=和hei= <span class="codeph"> 一 </span> 致 <span class="codeph"> 指定 </span>。 应用xScale和 <span class="varname"> yScale </span> 中 <span class="varname"> 的较 </span> 小者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 约束 </span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像， <span class="codeph"> 使其适应于分配 </span> wid=和wid=的空间，但实际响应可能比指定的wid=和hei=避 <span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> 免空间时的实际响应小。 应用xScale和 <span class="varname"> yScale </span> 中 <span class="varname"> 的较 </span> 小者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 裁切 </span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像，使其填充整个响应图像，并且裁切最少且没有空白。 应用 <span class="varname"> xScale和 </span> yScale <span class="varname"> 中较大 </span> 的值。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 换行 </span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像(如裁 <span class="codeph"> 切) </span> 以覆盖整个响应图像，但实际响应图像可能大于使用wid=和hei=指定的值 <span class="codeph"> ，以避 </span> 免裁 <span class="codeph"></span> 切。 应用 <span class="varname"> xScale和 </span> yScale <span class="varname"> 中的 </span>较大者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 拉伸 </span> </p> </td> 
   <td colname="col2"> <p>在x和y中独立缩放复合图像以填充整个响应图像，无需裁切和空白。 这通常会更改图像的长宽比。 <span class="varname"> xScale用 </span> 于水平缩放， <span class="varname"> yScale用 </span> 于垂直缩放。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 适合 </span> </p> </td> 
   <td colname="col2"> <p>应用 <span class="varname"> xScale </span> 以在水平方向上紧密调整图像，可能在顶部和／或底部裁剪或空白。 对于特殊应用程序有用。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>应用 <span class="varname"> yScale </span> 以垂直紧密调整图像，可能在左侧和／或右侧有裁剪或空白。 对于特殊应用程序有用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

设 *`upscale`* 置为“1”可允许升级，设置为“0”可限制*`xScale`* *`yScale`* 并限制为1:1。 如果禁用了上缩放，则复合图像小于响应图像时可能会存在额外的空白。

默认情况下，裁切和空白居中；他们的位置可以用来控制 `align=`。 空白填充的颜色和不透明度由决定 `bgc=`。

## 属性 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

视图属性。 无论当前图层设置如何，均可应用。 至少必须指定 `wid=` 或 `hei=` 者之一，否则将返回错误；必须 `wid=` 指定和 `hei=` 两者，才能使适合模式按说明行事。 当指定时， `req=tmb` 也会返回错误。

## 默认 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 另请参阅 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
