---
description: 使用Dynamic Media图像服务时，应考虑一些限制和已知问题。
solution: Experience Manager
title: 限制和已知问题
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 0%

---

# 限制和已知问题{#restrictions-and-known-issues}

使用Dynamic Media图像服务时，应考虑一些限制和已知问题。

## 文档勘误表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行数不超过`\copyfitmaxlines`设置的最大值和文本输入中的显式行数。
* 图像集中需要匹配的大括号和括号。 如果大括号与括号不匹配，则需要对URL进行编码。
* 服务器端全局响应时间警报包括错误响应。
* 将`id=`命令与图像或蒙版请求一起使用时，当前需要`rect=`命令。

## 已知差异textPs=与text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 合成斜体呈现的斜体比使用`text=`时少。
* 与使用`text=`时相比，下划线略低、略薄。
* `\expnd`和`\expndtw`与高负值一起使用，导致在使用`text=`时，字符被置于彼此前面。

* `\charscaley`与使用`text=`时的缩放不同，但不会影响行高。

* 如果文本的最后一行不适合，将放下整行，而不是显示为截止。
* `\slmult`和`\sl`的行为与MS Word和`text=`不同，它们只会对当前段落和后续段落生效。

* `\sb`应用于MS Word和`text=`的第一段，Adobe InDesign和[!DNL Photoshop]不执行此操作。

* `\sa`应用于MS Word和`text=`的最后一个段落，Adobe InDesign和[!DNL Photoshop]不执行此操作。

## 向后兼容性 {#section-a76842f751944f4fb664af296d064122}

* 在RTF字符串中转义下划线字符(`\_`)不适用于使用`textPs=`的所有字体

* 支持不区分大小写的宏处理。
* 目录缓存已从60秒减少到10秒。
* 错误重定向功能现在仅重定向引用目录中发布但在磁盘上未找到的损坏图像、字体、颜色配置文件和图像的请求。
* 如果任何修饰符值大于2147483648，`posN=`、`anchor=`、`anchorN=`、`origin=`和`originN=`现在将返回分析错误。

* 不支持嵌套请求的编码。 过渡到新行为，并对在网站的URL请求和公司目录中找到的任何嵌套请求值进行解码。
* 使用`req=tmb`时，DefaultImage现在应用缩略图属性。
* 在使用`flip=`的先前版本中，无论锚点是什么，图像从未重新定位。

## 适用于第三方库的限制 {#section-79768b96bf634e44ab672c5b893f343d}

如果已经检测到Digimarc水印，则Digimarc库拒绝对图像应用Digimarc水印。 如果对主图像进行了足够的编辑，则Digimarc库仍可以识别水印已应用。 但是，它可能不能读取该信息。 这会导致无法获得应用于原始图像的原始Digimarc信息的新图像。 图像服务现在可以应用在公司目录中定义的Digimarc水印。

## 适用于图像服务和图像渲染的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 当可用的CPU超过4个时，图像服务和图像渲染可能无法充分利用所有CPU。 在这些计算机上模拟您的通信量，以了解它在4个以上CPU方面的优势。
* 返回重定向的远程URL（HTTP状态301、302或303）会被拒绝。
* 在配置`errorRedirect.rootUrl`时，此属性中定义的IP地址需要包含在该服务器上的规则集`<addressfilter>`标记值中。

  *示例*：

  服务器A已定义`errorRedirect.rootUrl=10.10.10.10` 。

  IP地址为10.10.10.10的服务器B将规则集文件中的`<addressfilter>`标记值设置为包括其IP地址(10.10.10.10)。

* 具有定位的点文本和文本路径可能会显示剪切。
* `text=`仅将`\sa`和`\sb`应用于整个文本块，而不应用于每个段落。

* 使用在URL中定义的一个公司和为`src=`或`mask=`修饰符定义的另一个公司时，必须将正斜杠加到为`src=`或`mask=`定义的公司，此表单请求才能正常工作。

  *示例*：

  `/is/image/MyCompany?src=/YourCompany/MyImage` 。

  而不是： `/is/image/MyCompany?src=YourCompany/MyImage` 。

* 非金字塔Tiff或晕影请求会生成与类似的错误消息

  *“图像`C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`没有有效的DSF，且2.25MPixel的面积超过了最大值2MPixel”*。

  最佳实践是使用金字塔Tiff和晕影。 如果您需要使用非金字塔tiff或晕影，请按照下面的说明增加大小限制。

  *解决方法*：

  对于图像渲染的非金字塔晕影，请增加[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]配置文件中IrMaxNonPyrVignetteSize的属性值。

  对于图像服务非金字塔TIFF，在`MaxNonDsfSize`配置文件中增加[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]的属性值。

* 默认情况下，Adobe [!DNL Photoshop] CS3不会将分层的PSD文件保存为复合图像。

  *症状*：

  Adobe [!DNL Photoshop] CS3分层PSD文件显示为黑色，并带有文本声明：“此分层[!DNL Photoshop]文件未随复合图像一起保存。” 图像服务回复图像或IPS中的回复图像。

  *解決辦法*︰

  在启用了最大兼容性的情况下保存Adobe [!DNL Photoshop] CS3文件。

* 将ICC配置文件分配给CMYK/JPEG回复图像会导致某些浏览器中的颜色反转。*解决方法*：

  使用`fmt=`更改回复图像格式

* 压缩后的HTTP响应图像数据（包括文件头）的大小限制为16 MB。
* “ ...” 不允许在HTTP请求的任何路径元素中使用。
* 卸载可能会从&#x200B;*[!DNL install_root]*&#x200B;或任何子文件夹中删除用户创建或修改的文件。 在卸载之前，将此类文件复制到其他位置。

## 仅适用于图像服务的限制 {#section-b08ad535e4454265b8157dec244c4faf}

* PhotoFont文本不支持RTF (`\cf`)命令中的前景颜色。
* 合成粗体、斜体和粗体/斜体时，由于PhotoFont文本出错，因此被拒绝。
* PhotoFont文本不支持垂直文本流。
* PhotoFont文本不支持16bpc PNG图像。
* 嵌入了颜色配置文件的PNG图像的颜色校正使用硬编码选项。 渲染意图是相对比色，并且已为PhotoFont文本打开黑场补偿。
* 在公司[!DNL ini]文件中启用区域设置翻译时，不支持基于文件的查找。
* 图像服务无法正确写入非闭合[!DNL Photoshop]路径。
* 图像服务当前不支持处理使用Adobe Media Encoder 4.0.1或更早版本导出的TIFF文件。 Adobe Media Encoder包含在Premiere Pro CS4、After Effects CS4和Creative Suite 4 Production Premium中。
* 将`text=`与自调整图层结合使用不支持使用多个设置进行行对齐的RTF字符串。

  *示例*

  RTF字符串不能对自调整大小的文本图层同时使用左右行对齐。

* SVG对于未嵌入到SVG文件中的引用字体的字体查找路径拥有自己的属性。

  *症状*

  包含字体定义的已渲染SVG图像使用的字体不正确。

  *解决方法*

  在`svgProvider.fontRoot=`中设置属性[!DNL install_root/ImageServing/conf/PlatformServer.conf]。

* 裁切当前使用`bgColor=`而不是`color=`来填充任何新扩展区域。

* 当`bgColor=`与涉及颜色配置文件的基色空间不匹配时，颜色转换可能不正确。
* 如果图层没有蒙版或Alpha数据，则不会呈现外层效果。

## 仅适用于图像渲染的限制 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 贴花和墙面材料无法移除。
* 纹理的大小相对于晕影视图的大小是有限的。 在极少数情况下，默认限制为视图大小的425%可能会干扰使用非常大的不可重复纹理的应用程序。 如果无法将应用程序或内容更改为在预定义限制内工作，则百分比可以按如下方式增加。 使用文本编辑器，打开[!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]，找到`IrMaxTextureSizeFactor`并输入新的百分比值。 此更改将立即生效，无需重新启动图像服务器。

* 即使设置了nocache标头，Netscape和Opera中的JavaScript引擎也会缓存响应数据。 这会干扰有状态请求的正常运行。

  *解决方法*

  将时间戳或其他唯一标识符附加到请求字符串，如`"&.ts=currentTime`。

## 仅适用于实用程序的限制 {#section-906a6b2378154b3da122b2332983f7a5}

使用`ImageConvert`停止时，`control-c`有时会因分段错误而崩溃。
