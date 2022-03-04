---
description: 使用Dynamic Media图像服务时，应考虑一些限制和已知问题。
solution: Experience Manager
title: 限制和已知问题
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '1229'
ht-degree: 0%

---

# 限制和已知问题{#restrictions-and-known-issues}

使用Dynamic Media图像服务时，应考虑一些限制和已知问题。

## 文档勘误表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行数不会超过 `\copyfitmaxlines` 设置和文本输入中显式行的数量。
* 图像集中需要匹配的大括号和圆括号。 如果大括号和圆括号不匹配，则需要对它们进行URL编码。
* 服务器端全局响应时间警报包含错误响应。
* 的 `id=` 命令当前在使用 `rect=` 命令。

## 已知区别textPs=与text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 与使用 `text=`.
* 与使用 `text=`.
* `\expnd` 和 `\expndtw` 与高负值一起使用时，会导致字符在使用 `text=`.

* `\charscaley` 与使用 `text=` 但不会影响行高。

* 如果文本的最后一行不适合，则整行将被删除，而不是显示为截止。
* `\slmult` 和 `\sl` 与MS Word和的行为不同 `text=`，则它们只对当前和后续段落生效。

* `\sb` 适用于MS Word和的第一段 `text=`、 Adobe InDesign和Photoshop不会这样做。

* `\sa` 适用于MS Word和的最后一段 `text=`、 Adobe InDesign和Photoshop不会这样做。

## 向后兼容性 {#section-a76842f751944f4fb664af296d064122}

* 转义下划线字符( `\_`)无法用于RTF字符串中的所有字体 `textPs=`

* 支持不区分大小写的宏处理。
* 目录缓存已从60秒减少到10秒。
* 现在，错误重定向功能只能重定向引用目录中发布但在磁盘上未找到的损坏图像、字体、颜色配置文件和图像的请求。
* `posN=`, `anchor=`, `anchorN=`, `origin=`和 `originN=` 现在，如果有任何修饰符值大于2147483648，则返回解析错误。

* 不支持嵌套请求的编码。 过渡到新行为，并取消对网站和公司目录中URL请求中找到的任何嵌套请求值的编码。
* DefaultImage现在在使用 `req=tmb`.
* 在以前的版本中，使用 `flip=`，则无论锚点是什么，都不会重新定位图像。

## 适用于第三方库的限制 {#section-79768b96bf634e44ab672c5b893f343d}

如果已检测到Digimarc水印，则Digimarc库拒绝将Digimarc水印应用于图像。 如果对主图像进行了足够的编辑，Digimarc库仍可能能够识别已应用水印。 但是，它可能无法读取该信息。 这会产生一个新图像，其中无法获得应用于原始图像的原始Digimarc信息。 图像提供功能现在可以应用公司目录中定义的Digimarc水印。

## 适用于图像提供和图像呈现的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 当有4个以上的CPU可用时，图像提供和图像呈现可能无法充分利用所有CPU。 在这些计算机上模拟流量，以了解4个以上CPU的优势。
* 返回重定向的远程URL（HTTP状态301、302或303）将被拒绝。
* 配置时 `errorRedirect.rootUrl` 此属性中定义的IP地址需要包含在规则集中 `<addressfilter>` 标记值。

   *示例*:

   服务器A已定义 `errorRedirect.rootUrl=10.10.10.10` .

   IP地址为10.10.10.10的服务器B将 `<addressfilter>` 标记值以包含其IP地址(10.10.10.10)。

* 具有定位的点文本和文本路径可能显示剪切。
* `text=` 仅适用 `\sa` 和 `\sb` 到整个文本块，而不是按段落。

* 使用URL中定义的一家公司和为 `src=` 或 `mask=` 修饰符，则必须在为 `src=` 或 `mask=` 以使这种形式的请求生效。

   *示例*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   而不是： `/is/image/MyCompany?src=YourCompany/MyImage` .

* 非吡唑化的Tiff或晕影请求会生成类似于

   *&quot;图像 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 没有有效的DSF，面积2.25MPixel超过2MPixel的最大值”* .

   最佳做法是使用带图像的Tiff和Vignet。 如果您需要使用非图形化的tiff或晕影，请按照以下说明提高大小限制。

   *周旋*:

   对于图像渲染非金字塔晕影，请在 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 配置文件。

   对于图像提供非金字塔TIFF，请增加 `MaxNonDsfSize` 在 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 配置文件。

* Adobe Photoshop CS3默认不保存复合图像的分层PSD文件。

   *症状*:

   Adobe Photoshop CS3分层PSD文件显示为黑色，并且文本中写明“此分层Photoshop文件未与复合图像一起保存。” （在IPS中）。

   *解決辦法*︰

   保存Adobe Photoshop CS3文件，同时最大限度地启用兼容性。

* 将ICC配置文件分配给CMYK/JPEG回复图像会导致某些浏览器中的颜色反转。*周旋*:

   使用更改回复图像格式 `fmt=`

* 压缩后的HTTP响应图像数据（包括文件头）的大小限制为16 MB。
* &quot;。.&quot; 在HTTP请求中的任何路径元素中均不允许使用。
* 卸载操作可从 *[!DNL install_root]* 或任何子文件夹。 在卸载之前，将此类文件复制到其他位置。

## 仅适用于图像提供的限制 {#section-b08ad535e4454265b8157dec244c4faf}

* RTF中的前台颜色( `\cf`)命令。
* 合成粗体、斜体和粗体/斜体将作为PhotoFont文本的错误而被拒绝。
* PhotoFont文本不支持垂直文本流。
* PhotoFont文本不支持16bpc PNG图像。
* 嵌入了颜色配置文件的PNG图像的颜色校正使用硬编码选项。 呈现意图是相对比色的，并且为PhotoFont文本打开黑点补偿。
* 在公司中启用区域设置转换时，不支持基于文件的查找 [!DNL ini] 文件。
* 图像提供无法正确写入非关闭的Photoshop路径。
* 图像服务当前不支持处理使用Adobe Media Encoder 4.0.1或更低版本导出的TIFF文件。 Adobe Media Encoder随Premiere ProCS4、After Effects CS4和Creative Suite4 Production Premium一起提供。
* 使用 `text=` 自调整层大小不支持使用多个设置进行行对齐的RTF字符串。

   *示例*

   RTF字符串不能对自调整文本层大小时同时使用左行和右行对齐。

* SVG对于未嵌入SVG文件中的引用字体的字体查找路径，具有其自身的属性。

   *症状*

   包含字体定义的已渲染SVG图像使用的字体不正确。

   *解决方法*

   设置属性 `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* 裁切当前正在使用 `bgColor=` 而不是 `color=` 来填充任何新扩展的区域。

* 颜色转换在 `bgColor=` 与涉及颜色配置文件的基本颜色空间不匹配。
* 如果图层没有蒙版或Alpha数据，则不会呈现外层效果。

## 仅适用于图像渲染的限制 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 壁板和壁材不可拆卸。
* 纹理的大小相对于晕影视图的大小是有限的。 在极少数情况下，视图大小的425%的默认限制可能会妨碍使用非常大的非可重复纹理的应用程序。 如果无法在预定义的限制范围内更改应用程序或内容以正常工作，则百分比可以按如下方式增加。 使用文本编辑器，打开 [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]，查找 `IrMaxTextureSizeFactor` 并输入新的百分比值。 更改将立即生效，而不重新启动图像服务器。

* 即使设置了nocache标头，Netscape和Opera中的JavaScript引擎也会缓存响应数据。 这会干扰有状态请求的正常运行。

   *解决方法*

   将时间戳或其他唯一标识符附加到请求字符串，例如 `"&.ts=currentTime`.

## 仅适用于实用工具的限制 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`当使用 `control-c`.
