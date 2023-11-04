---
description: 使用Dynamic Media图像服务时，应考虑一些限制和已知问题。
solution: Experience Manager
title: 限制和已知问题
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1221'
ht-degree: 0%

---

# 限制和已知问题{#restrictions-and-known-issues}

使用Dynamic Media图像服务时，应考虑一些限制和已知问题。

## 文档勘误表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行数不超过 `\copyfitmaxlines` 设置文本输入中的显式行数。
* 图像集中需要匹配的大括号和括号。 如果大括号与括号不匹配，则需要对URL进行编码。
* 服务器端全局响应时间警报包括错误响应。
* 此 `id=` 命令当前在使用时 `rect=` 命令中的图像或掩码请求。

## 已知差异textPs=与text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 合成斜体呈现的倾斜度比使用时小 `text=`.
* 下划线比使用时更小、更薄 `text=`.
* `\expnd` 和 `\expndtw` 与高负值一起使用，会导致在使用时，字符被放置到彼此的前面 `text=`.

* `\charscaley` 刻度与使用时不同 `text=` 但不影响线条高度。

* 如果文本的最后一行不适合，将放下整行，而不是显示为截止。
* `\slmult` 和 `\sl` 行为与MS Word和 `text=`，它们只会对当前段落和后续段落生效。

* `\sb` 适用于MS Word和的第一段 `text=`、Adobe InDesign和 [!DNL Photoshop] 别这样。

* `\sa` 适用于MS Word和的最后一个段落 `text=`、Adobe InDesign和 [!DNL Photoshop] 别这样。

## 向后兼容性 {#section-a76842f751944f4fb664af296d064122}

* 转义下划线字符( `\_`)，不能与使用的所有字体一起使用 `textPs=`

* 支持不区分大小写的宏处理。
* 目录缓存已从60秒减少到10秒。
* 错误重定向功能现在仅重定向引用目录中发布但在磁盘上未找到的损坏图像、字体、颜色配置文件和图像的请求。
* `posN=`， `anchor=`， `anchorN=`， `origin=`、和 `originN=` 现在，如果任何修饰符值大于2147483648，则返回分析错误。

* 不支持嵌套请求的编码。 过渡到新行为，并对在网站的URL请求和公司目录中找到的任何嵌套请求值进行解码。
* 现在，DefaultImage在使用时应用缩略图属性 `req=tmb`.
* 在以前的版本中，使用 `flip=`，无论锚点是什么，都不会重新定位图像。

## 适用于第三方库的限制 {#section-79768b96bf634e44ab672c5b893f343d}

如果已经检测到Digimarc水印，则Digimarc库拒绝对图像应用Digimarc水印。 如果对主图像进行了足够的编辑，则Digimarc库仍可以识别水印已应用。 但是，它可能不能读取该信息。 这会导致无法获得应用于原始图像的原始Digimarc信息的新图像。 图像服务现在可以应用在公司目录中定义的Digimarc水印。

## 适用于图像服务和图像渲染的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 当可用的CPU超过4个时，图像服务和图像渲染可能无法充分利用所有CPU。 在这些计算机上模拟您的通信量，以了解它在4个以上CPU方面的优势。
* 返回重定向的远程URL（HTTP状态301、302或303）会被拒绝。
* 配置时 `errorRedirect.rootUrl` 此属性中定义的IP地址需要包含在规则集中 `<addressfilter>` 标记值。

  *示例*:

  服务器A已定义 `errorRedirect.rootUrl=10.10.10.10` .

  IP地址为10.10.10.10的服务器B设置 `<addressfilter>` 规则集文件中的标记值包含其IP地址(10.10.10.10)。

* 具有定位的点文本和文本路径可能会显示剪切。
* `text=` 仅适用 `\sa` 和 `\sb` 整个文本块而不是每个段落。

* 使用URL中定义的一家公司和为定义的另一家公司时 `src=` 或 `mask=` 修饰符，您必须在为定义的公司添加正斜杠前缀 `src=` 或 `mask=` 才能使此形式的请求正常工作。

  *示例*:

  `/is/image/MyCompany?src=/YourCompany/MyImage` .

  而非： `/is/image/MyCompany?src=YourCompany/MyImage` .

* 非金字塔Tiff或晕影请求会生成与类似的错误消息

  *&quot;图像 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 没有有效的DSF，且2.25MPixel的面积超过了最大值2MPixel”* .

  最佳实践是使用金字塔Tiff和晕影。 如果您需要使用非金字塔tiff或晕影，请按照下面的说明增加大小限制。

  *解决方法*：

  对于图像渲染的非金字塔晕影，请将IrMaxNonPyrVignetteSize的属性值增加到 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 配置文件。

  对于图像服务非金字塔TIFF，增加以下属性的值 `MaxNonDsfSize` 在 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 配置文件。

* Adobe [!DNL Photoshop] 默认情况下，CS3不保存分层PSD文件为复合图像。

  *症状*：

  Adobe [!DNL Photoshop] CS3分层PSD文件显示为黑色，文本显示“此分层 [!DNL Photoshop] 文件未与复合图像一起保存。” 图像服务回复图像或IPS中的回复图像。

  *解決辦法*︰

  保存Adobe [!DNL Photoshop] 已启用最大兼容性的CS3文件。

* 将ICC配置文件分配给CMYK/JPEG回复图像会导致某些浏览器中的颜色反转。*解决方法*：

  更改回复图像格式，使用 `fmt=`

* 压缩后的HTTP响应图像数据（包括文件头）的大小限制为16 MB。
* “ ...” 不允许在HTTP请求的任何路径元素中使用。
* 卸载可能会从中删除用户创建或修改的文件 *[!DNL install_root]* 或任何子文件夹。 在卸载之前，将此类文件复制到其他位置。

## 仅适用于图像服务的限制 {#section-b08ad535e4454265b8157dec244c4faf}

* RTF中的前景色( `\cf`)命令不支持PhotoFont文本。
* 合成粗体、斜体和粗体/斜体时，由于PhotoFont文本出错，因此被拒绝。
* PhotoFont文本不支持垂直文本流。
* PhotoFont文本不支持16bpc PNG图像。
* 嵌入了颜色配置文件的PNG图像的颜色校正使用硬编码选项。 渲染意图是相对比色，并且已为PhotoFont文本打开黑场补偿。
* 在公司中启用区域设置翻译时，不支持基于文件的查找 [!DNL ini] 文件。
* 图像服务不会写入未关闭的内容 [!DNL Photoshop] 路径正确。
* 图像服务当前不支持处理使用Adobe Media Encoder 4.0.1或更早版本导出的TIFF文件。 Adobe Media Encoder包含在Premiere ProCS4、After Effects CS4和Creative Suite4 Production Premium中。
* 使用 `text=` 使用自调整大小的图层不支持使用多个设置进行行对齐的RTF字符串。

  *示例*

  RTF字符串不能对自调整大小的文本图层同时使用左右行对齐。

* 对于未嵌入到SVG文件中的所引用SVG的字体查找路径，字体具有其自己的属性。

  *症状*

  包含字体定义的渲染SVG图像使用的字体不正确。

  *解决方法*

  设置属性 `svgProvider.fontRoot=` 在 [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* 裁切当前正在使用 `bgColor=` 而不是 `color=` 以填充任何新扩展区域。

* 在以下情况下，颜色转换可能不正确 `bgColor=` 不匹配涉及颜色配置文件的基本颜色空间。
* 如果图层没有蒙版或Alpha数据，则不会呈现外层效果。

## 仅适用于图像渲染的限制 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 贴花和墙面材料无法移除。
* 纹理的大小相对于晕影视图的大小是有限的。 在极少数情况下，默认限制为视图大小的425%可能会干扰使用非常大的不可重复纹理的应用程序。 如果无法将应用程序或内容更改为在预定义限制内工作，则百分比可以按如下方式增加。 使用文本编辑器，打开 [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]，查找 `IrMaxTextureSizeFactor` 并输入新的百分比值。 此更改将立即生效，无需重新启动图像服务器。

* Netscape和Opera中的JavaScript引擎缓存响应数据，即使设置了nocache标头也是如此。 这会干扰有状态请求的正常运行。

  *解决方法*

  将时间戳或其他唯一标识符附加到请求字符串，例如 `"&.ts=currentTime`.

## 仅适用于实用程序的限制 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`在使用停止时，有时会由于分段错误而崩溃 `control-c`.
