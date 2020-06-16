---
description: 使用Scene7图像服务时，应考虑一些限制和已知问题。
seo-description: 使用Scene7图像服务时，应考虑一些限制和已知问题。
seo-title: 限制和已知问题
solution: Experience Manager
title: 限制和已知问题
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---


# 限制和已知问题{#restrictions-and-known-issues}

使用Scene7图像服务时，应考虑一些限制和已知问题。

## 文档勘误表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行数不会超过文本输入中 `\copyfitmaxlines` 设置和显式行数的最大值。
* 图像集中需要匹配的大括号和圆括号。 如果大括号和圆括号不匹配，则需要对它们进行URL编码。
* 服务器端全局响应时间警报包括错误响应。
* 当 `id=` 前，对图像或蒙版请求 `rect=` 使用命令时，该命令是必需的。

## 已知差异文本Ps=与文本= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 合成斜体的倾斜程度比使用时要小 `text=`。
* 下划线比使用时稍低和更薄 `text=`。
* `\expnd` 与 `\expndtw` 高负值一起使用时，会导致字符在使用时彼此前排 `text=`。

* `\charscaley` 缩放方式与使用方式不 `text=` 同，但不会影响行高。

* 如果最后一行文本不适合，整个行将丢弃，而不显示为截止。
* `\slmult` 并且 `\sl` 其行为方式与MS Word不同 `text=`，它们只会对当前和后续段落生效。

* `\sb` 适用于MS Word和Adobe InDesign `text=`和Photoshop的第一段落，但不适用。

* `\sa` 适用于MS Word和Adobe InDesign `text=`和Photoshop的最后一段。

## 向后兼容性 {#section-a76842f751944f4fb664af296d064122}

* 在RTF字符串中转 `\_`义下划线字符()不能使用所有字体 `textPs=`

* 支持不区分大小写的宏处理。
* 目录缓存已从60秒减少到10秒。
* 错误重定向功能现在仅重定向引用损坏的图像、字体、颜色用户档案和在目录中发布但在磁盘上找不到的图像的请求。
* `posN=`、 `anchor=`、 `anchorN=`、和现在 `origin=``originN=` ，如果任何修饰符值大于2147483648，则返回解析错误。

* 不支持嵌套请求的编码。 过渡到新行为，并取消对您站点和公司目录中URL请求中的任何嵌套请求值的编码。
* 现在，DefaultImage在使用时应用缩略图属 `req=tmb`性。
* 在使用的先 `flip=`前版本中，无论锚点是什么，都不会重新定位图像。

## 适用于第三方库的限制 {#section-79768b96bf634e44ab672c5b893f343d}

如果已检测到图像，Digimarc库拒绝将Digimarc水印应用于图像。 如果对主图像进行了足够的编辑，Digimarc库仍可识别已应用水印。 但是，它可能无法读取该信息。 这会产生一个新图像，在该新图像中，无法获得应用于原始图像的原始Digimarc信息。 图像服务现在可以应用在公司目录中定义的Digimarc水印。

## 适用于图像服务和图像渲染的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 当超过4个CPU可用时，图像服务和图像渲染可能不会充分利用所有CPU。 在这些计算机上模拟流量，了解4个以上CPU的优势。
* 返回重定向的远程URL（HTTP状态301、302或303）被拒绝。
* 配置此 `errorRedirect.rootUrl` 属性中定义的IP地址时，需要将其包括在该服务器上的 `<addressfilter>` 规则集标记值中。

   *示例*:

   服务器A已定义 `errorRedirect.rootUrl=10.10.10.10` 。

   服务器B的IP地址为10.10.10.10，在规则集文件中 `<addressfilter>` 设置标记值以包含其IP地址(10.10.10.10)。

* 具有定位的点文本和文本路径可能显示剪切。
* `text=` 仅应用于 `\sa` 整个 `\sb` 文本块，而不是每个段落。

* 当使用URL中定义的公司和为该或修饰符定义的 `src=` 其他公司 `mask=` 时，您必须在为此形式的请求定义的公司或为该形式的请求定义的前 `src=``mask=` 加一个正斜杠。

   *示例*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   而不是： `/is/image/MyCompany?src=YourCompany/MyImage` .

* 非吡唑化Tiff或暗角请求会生成类似的错误消息，

   *“图`C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`像没有有效的DSF,2.25MPixel的面积超过2MPixel的最大面积* 。”

   最佳做法是使用吡喃Tiff和晕影。 如果您需要使用非吡喃藏獒或晕影，请按照以下说明增加大小限制。

   *解决问题*:

   对于图像渲染非吡唑化晕影，请增加[!DNL/ImageServing/bin/ ImageServerRegistry.xml]配 *[!DNL install_root]*&#x200B;置文件中IrMaxNonPyrVignetteSize的属性值。

   对于未吡唑化的TIFF图像服务，请增 `MaxNonDsfSize` 加[!DNL *[!DNL install_root]* /ImageServing/bin/ ImageServerRegistry.xml]配置文件的属性值。

* 默认情况下，Adobe Photoshop CS3不保存图层式PSD文件，即合成图像。

   *症状*:

   Adobe Photoshop CS3分层PSD文件显示为黑色，并显示文本声明：“此分层Photoshop文件未与复合图像一起保存。” （在IPS中）。

   *解決辦法*︰

   打开最大兼容性时保存Adobe Photoshop CS3文件。

* 将ICC用户档案指定给CMYK/JPEG回复图像会导致某些浏览器中的颜色发生反转。*解决问题*:

   使用 `fmt=`

* 压缩后HTTP响应图像数据（包括文件头）的大小限制为16 MB。
* &quot; ..&quot; 不允许在HTTP请求中的任何路径元素中使用。
* 卸载可从或任何子文件夹删除用户创建 *[!DNL install_root]* 或修改的文件。 卸载前将这些文件复制到其他位置。

## 限制仅适用于图像服务 {#section-b08ad535e4454265b8157dec244c4faf}

* PhotoFont文本不支持RTF( `\cf`)命令中的前景色。
* 合成粗体、斜体和粗体／斜体将作为PhotoFont文本的错误被拒绝。
* PhotoFont文本不支持垂直文本排列。
* PhotoFont文本不支持16bpc PNG图像。
* 嵌入了颜色用户档案的PNG图像的颜色校正使用硬编码选项。 渲染意图是相对比色的，并且PhotoFont文本的黑点补偿处于开启状态。
* 在公司文件中启用区域设置转换时，不支持基于文件的 [!DNL ini] 查找。
* 图像服务无法正确写入非闭合的Photoshop路径。
* 图像服务当前不支持处理使用Adobe Media Encoder 4.0.1或更早版本导出的TIFF文件。 Premiere Pro CS4、After Effects CS4和Creative Suite 4 Production Premium包含Adobe Media Encoder。
* 在自 `text=` 动调整图层大小时使用不支持使用多个行对齐设置的RTF字符串。

   *示例*

   RTF字符串不能对自调整大小的文本图层同时使用左行和右行对齐。

* SVG对于未嵌入SVG文件的引用字体的字体查找路径具有自己的属性。

   *症状*

   呈现的包含字体定义的SVG图像使用的字体不正确。

   *解决方法*

   在[!DNL `svgProvider.fontRoot=` /ImageServing/conf/PlatformServer.conf]中 *[!DNL install_root]* 设置属性。

* 当前使用裁切 `bgColor=` 而不是 `color=` 填充任何新扩展区域。

* 当与涉及颜色用户档案的基色空 `bgColor=` 间不匹配时，颜色转换可能不正确。
* 如果图层没有蒙版或alpha数据，则不渲染外层效果。

## 限制仅适用于图像渲染 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 壁板和壁材无法拆卸。
* 纹理的大小相对于暗角视图的大小是有限的。 在极少的情况下，默认限制为视图大小的425%可能会干扰使用大型非可重复纹理的应用程序。 如果无法将应用程序或内容更改为在预定义的限制范围内工作，则百分比可以增加如下。 使用文本编辑器打开[! *[!DNL install_root]* DNL /ImageServing/conf/ImageServerRegistry.xml]，找 `IrMaxTextureSizeFactor` 到并输入新的百分比值。 更改将立即生效，无需重新启动图像服务器。

* Netscape和Opera缓存响应数据中的JavaScript引擎，即使已设置nocache头。 这妨碍了有国家要求的正常运行。

   *解决方法*

   将时间戳或其他唯一标识符追加到请求字符串，如 `"&.ts=currentTime`。

## 限制仅适用于实用程序 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`有时，当停止时会因分段错误而崩溃 `control-c`。
