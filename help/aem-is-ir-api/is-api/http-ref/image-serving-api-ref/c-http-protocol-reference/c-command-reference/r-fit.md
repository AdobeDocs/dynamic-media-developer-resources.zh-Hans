---
title: 适合
description: 响应图像拟合模式。 指定缩放因子的计算方式，当使用wid=和hei=和scl=指定响应大小时，缩放因子用于将复合图像缩放到响应图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 2%

---

# 适合{#fit}

响应图像拟合模式。 指定缩放因子的计算方式，当使用wid=和hei=和scl=指定响应大小时，缩放因子用于将复合图像缩放到响应图像。

` fit= *`模式`*, *`高档`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 模式 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 拟合|约束|裁剪|包裹|拉伸|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 高档 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

在以下模式选项描述中，假定 *`xScale`* 是复合图像宽度与响应图像宽度和 *`yScale`* 是复合图像高度与响应图像高度的比值。

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
   <td colname="col2"> <p>缩放复合图像，使其适合分配的空间 <span class="codeph"> wid= </span> 和 <span class="codeph"> hei= </span>，具有最小的空白空间且不会裁剪。 响应图像的大小将与 <span class="codeph"> wid= </span> 和 <span class="codeph"> hei= </span>. 小于 <span class="varname"> xScale </span> 和 <span class="varname"> yScale </span> 的次数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 约束 </span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像，如 <span class="codeph"> 拟合 </span> 这样它就能被放入 <span class="codeph"> wid= </span> 和 <span class="codeph"> hei= </span>，但实际响应图像可能比 <span class="codeph"> wid= </span> 和 <span class="codeph"> hei= </span> 以避免空白。 小于 <span class="varname"> xScale </span> 和 <span class="varname"> yScale </span> 的次数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 裁切 </span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像，以便它以最小的裁剪和没有空格的方式填充整个响应图像。 大 <span class="varname"> xScale </span> 和 <span class="varname"> yScale </span> 的次数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 换行 </span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像，如 <span class="codeph"> 农作物 </span> 以便覆盖整个响应图像，但实际响应图像可能比指定的大 <span class="codeph"> wid= </span> 和 <span class="codeph"> hei= </span> 避免裁剪。 大 <span class="varname"> xScale </span> 和 <span class="varname"> yScale </span>的次数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 拉伸 </span> </p> </td> 
   <td colname="col2"> <p>单独按x和y缩放复合图像，以填充整个响应图像，无需裁剪和空格。 这通常会更改图像的宽高比。 <span class="varname"> xScale </span> 用于水平缩放和 <span class="varname"> yScale </span> 垂直缩放。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>应用 <span class="varname"> xScale </span> 以水平紧凑地调整图像大小，可能会在顶部和/或底部裁剪或空格。 对特殊应用程序非常有用。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>应用 <span class="varname"> yScale </span> 可垂直紧贴图像，并在左侧和/或右侧可能裁剪或空格。 对特殊应用程序非常有用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

已设置 *`upscale`* 为“1”以允许缩放，或限制为“0”*`xScale`*和 *`yScale`* 限制为1:1。 如果禁用了上缩放，则如果复合图像小于响应图像，则可能存在额外的空格。

默认情况下，裁切和空格居中；通过 `align=`. 空格填充的颜色和不透明度由 `bgc=`.

## 属性 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

查看属性。 无论当前的层设置如何，都适用。 至少其中一个 `wid=` 或 `hei=` 必须同时指定，否则返回错误；both `wid=` 和 `hei=` 必须为要按说明行为的适合模式指定。 在 `req=tmb` 也指定了。

## 默认 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 另请参阅 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
