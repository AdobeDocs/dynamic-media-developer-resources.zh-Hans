---
description: 图像服务支持将可缩放矢量图形(SVG)文件作为源数据。 必须符合SVG1.1。
solution: Experience Manager
title: SVG支持
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# SVG支持{#svg-support}

图像服务支持将可缩放矢量图形(SVG)文件作为源数据。 必须符合SVG1.1。

图像提供仅识别静态SVG内容；不支持动画、脚本和其他交互式内容。

SVG可以在允许图像文件的位置指定(URL路径、 `src=`和 `mask=`)。 SVG文件的内容栅格化后，其处理方式与图像类似。

与图像类似，SVG文件可以指定为图像目录条目或相对文件路径。

## 替换变量 {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 替换变量可能包含在值字符串的SVG文件中 `<text>` 元素和任何元素属性。

嵌入式图像服务请求的查询部分中的重要变量不会直接替换。 相反，所有可用的变量定义都会附加到请求中，这允许图像服务在解析请求时替换变量。

请参阅 [替换变量](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) 以了解其他信息。

## 图像引用 {#section-a7680f9e6aca4b1a83560637cc9fac66}

可以使用将图像插入到SVG中 `<image>` 元素。 由 `xlink::href` 属性 `<image>` 元素必须是有效的图像服务请求。 不允许使用外国URL。

指定完整的图像提供请求，以开始 `http://`，或相对url，以开头 `/is/image`. 如果指定了完整的HTTP路径，则会从路径中删除域名，以将其转换为相对格式。 使用完整的HTTP路径可能会有好处，因为它允许使用第三方SVG渲染器预览文件。

>[!NOTE]
>
>在此版本的“图像提供”中，对渲染图像的支持受到限制。 仅在传统图像提供分层和模板机制不足以达到预期结果的情况下，才应使用SVG内引用图像。 在任何情况下都不应使用SVG来生成多图像复合。

>[!NOTE]
>
>此时不会自动调整SVG中嵌入的图像大小。 确保所有图像参数都包含必要的“图像提供”命令，以设置所需的图像大小(例如， `wid=`)。 如果未明确设置图像大小， `attribute::DefaultPix` 的次数。

## 色彩管理 {#section-ea76e2bc4e1842638aa97a2d470c8a68}

所有嵌入在SVG文件中并通过替换变量传递到SVG模板的颜色值都假定存在于 `sRgb` 色彩空间。

将图像嵌入到SVG中后，不执行颜色转换。 要确保颜色保真度，请确保指定 `icc=sRgb` 适用于所有嵌入的图像请求。

光栅化后，SVG图像与任何其他图像一样参与色彩管理。

## 示例 {#section-036cdd45abd449849ee00a8f21788c28}

以下SVG模板说明了图像引用和变量的使用。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

此SVG模板的使用方式如下：

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 限制 {#section-daa5eccd07204aaf993be41e87822d54}

SVG文件必须独立，且不得引用任何辅助文件或资源，但与图像提供或图像渲染请求一起引用的外部图像除外（请参阅上文）。

仅呈现静态内容。 动画、交互功能（如按钮等） 可能存在，但可能无法按预期呈现。

目前不支持基于ICC配置文件的颜色规范。

`<script>` 元素可能存在，但始终会被忽略。

## 另请参阅 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [掩码=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG1.1规范](https://www.w3.org/TR/SVG11/)
