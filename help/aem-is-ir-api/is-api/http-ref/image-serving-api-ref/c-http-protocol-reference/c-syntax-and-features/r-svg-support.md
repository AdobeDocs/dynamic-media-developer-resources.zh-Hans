---
description: 图像服务支持可缩放矢量图形(SVG)文件作为源数据。 需要符合SVG 1.1。
seo-description: 图像服务支持可缩放矢量图形(SVG)文件作为源数据。 需要符合SVG 1.1。
seo-title: SVG支持
solution: Experience Manager
title: SVG支持
uuid: 30d7b37d-fdef-4518-a4b3-4baee56fa634
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---


# SVG支持{#svg-support}

图像服务支持可缩放矢量图形(SVG)文件作为源数据。 需要符合SVG 1.1。

图像服务仅识别静态SVG内容；不支持动画、脚本和其他交互式内容。

可以在允许图像文件（URL路径、`src=`和`mask=`）的任何位置指定SVG。 栅格化SVG文件的内容后，它就像处理图像一样处理。

与图像类似，SVG文件可以指定为图像目录条目或相对文件路径。

## 替换变量{#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` 替换变量可以包括在值字符串元素和任何 `<text>` 元素属性中的SVG文件中。

嵌入式图像服务请求的查询部分中的重要变量不会直接替换。 相反，所有可用的变量定义都会附加到请求中，这样，图像服务就可以在分析请求时替换变量。

有关其他信息，请参阅[替换变量](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)。

## 图像引用{#section-a7680f9e6aca4b1a83560637cc9fac66}

可以使用`<image>`元素将图像插入SVG。 由`<image>`元素的`xlink::href`属性引用的图像必须是有效的图像服务请求。 不允许使用外国URL。

指定完整的图像服务请求（从`http://`开始）或相对url（从`/is/image`开始）。 如果指定了完整的HTTP路径，则将从路径中删除域名，以转换为相对格式。 使用完整的HTTP路径可能有好处，因为它允许使用第三方SVG渲染器预览文件。

>[!NOTE]
>
>此版本图像服务中对渲染图像的支持有限。 仅在传统图像服务分层和模板机制不足以达到预期效果的情况下，应使用SVG中引用图像。 在任何情况下都不应使用SVG生成多图像复合。

>[!NOTE]
>
>此时，嵌入到SVG中的图像不会自动调整大小。 确保所有图像参数都包含必要的“图像服务”命令以设置所需的图像大小(例如，`wid=`)。 如果未显式设置图像大小，则将应用`attribute::DefaultPix`。

## 色彩管理{#section-ea76e2bc4e1842638aa97a2d470c8a68}

所有嵌入在SVG文件中并通过替换变量传递到SVG模板的颜色值都假定存在于`sRgb`色彩空间中。

当图像嵌入到SVG中时，不执行颜色转换。 要确保颜色保真度，请确保为所有嵌入的图像请求指定`icc=sRgb`。

栅格化后，SVG图像与任何其他图像一样参与色彩管理。

## 示例 {#section-036cdd45abd449849ee00a8f21788c28}

以下SVG模板说明了图像引用和变量的使用。

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

此SVG模板可能使用如下：

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## 限制{#section-daa5eccd07204aaf993be41e87822d54}

SVG文件必须是独立的，不得引用任何辅助文件或资源，但“图像服务”或“图像渲染”请求引用的外部图像除外（请参阅上文）。

只渲染静态内容。 动画、交互功能，如按钮等。 可能存在，但可能无法按预期呈现。

目前不支持基于ICC用户档案的颜色规范。

`<script>` 元素可能存在，但始终被忽略。

## 另请参阅 {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [ mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [SVG 1.1规范](http://www.w3.org/TR/SVG11/)
