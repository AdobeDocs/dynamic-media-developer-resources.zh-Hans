---
title: 适合
description: 响应图像适应模式。 指定如何计算缩放因子，当使用wid=指定响应大小且不存在hei=和scl=时，该因子用于将复合图像缩放为响应图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# 适合{#fit}

响应图像适应模式。 指定如何计算缩放因子，当使用wid=指定响应大小且不存在hei=和scl=时，该因子用于将复合图像缩放为响应图像。

` fit= *`模式`*, *`升级`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">模式</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|约束|裁切|换行|延伸|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">升级</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

在模式选项的以下描述中，假定&#x200B;*`xScale`*&#x200B;是复合图像宽度与响应图像宽度的比率，*`yScale`*&#x200B;是复合图像高度与响应图像高度的比率。

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 参数 </th> 
   <th colname="col2" class="entry"> 定义 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">适合</span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像，使其适应分配为<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>的空间，并且只有最少的空格且无裁切。 响应图像具有指定的精确大小，其中<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>。 已应用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>中的较小者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">约束</span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像（如<span class="codeph">适合</span>），使其适合使用<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>分配的空间，但实际响应图像可能小于使用<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>指定的空间，以避免留空白。 已应用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>中的较小者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">裁切</span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像，以填充整个响应图像，同时尽量减少裁剪并且不留空格。 已应用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>中的较大者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">自动换行</span> </p> </td> 
   <td colname="col2"> <p>缩放复合图像（如<span class="codeph">裁切</span>），使其覆盖整个响应图像，但实际响应图像可能大于使用<span class="codeph"> wid= </span>和<span class="codeph"> hei= </span>指定的值，以避免裁切。 已应用<span class="varname"> xScale </span>和<span class="varname"> yScale </span>中的较大者。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">延伸</span> </p> </td> 
   <td colname="col2"> <p>在x和y中独立缩放复合图像以填充整个响应图像，无裁剪和无空格。 这通常会更改图像的纵横比。 <span class="varname"> xScale </span>用于水平缩放，<span class="varname"> yScale </span>用于垂直缩放。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>应用<span class="varname"> xScale </span>以水平紧密配合图像，可能在顶部和/或底部裁切或留空白。 对于特殊应用很有用。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>应用<span class="varname"> yScale </span>以垂直紧密配合图像，可能在左侧和/或右侧裁切或留空白。 对于特殊应用很有用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

将&#x200B;*`upscale`*&#x200B;设置为“1”以允许升级，或设置为“0”以限制*`xScale`*并将&#x200B;*`yScale`*&#x200B;限制为1:1。 如果禁用了升级，则如果复合图像小于响应图像，则可能会显示额外的空白。

默认情况下，将裁切和空格居中；可以使用`align=`控制其位置。 空白填充的颜色和不透明度由`bgc=`决定。

## 属性 {#section-6d7a5a7e18434bca9bc2fdb236af8909}

查看属性。 无论当前图层设置如何，均适用。 还必须至少指定`wid=`或`hei=`之一，否则将返回错误；必须指定`wid=`和`hei=`才能使适合模式按所述运行。 同时指定了`req=tmb`时返回错误。

## 默认 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 另请参阅 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
