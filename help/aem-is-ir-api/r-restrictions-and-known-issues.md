---
description: 使用Dynamic Media图像服务时，应考虑一些限制和已知问题。
solution: Experience Manager
title: 限制和已知问题
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1238'
ht-degree: 0%

---


# 限制和已知问题{#restrictions-and-known-issues}

使用Dynamic Media图像服务时，应考虑一些限制和已知问题。

## 文档勘误表{#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行数不会超过文本输入中`\copyfitmaxlines`设置的最大值和显式行数。
* 图像集中需要匹配的大括号和小括号。 如果大括号和小括号不匹配，则需要对它们进行URL编码。
* 服务器端全局响应时间警报包括错误响应。
* 当前，对图像或蒙版请求使用`rect=`命令时，需要`id=`命令。

## 已知差异textPs=与text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 与使用`text=`时相比，合成斜体的倾斜程度要小。
* 与使用`text=`时相比，下划线有点低和更薄。
* `\expnd` 和 `\expndtw` 与高负值一起使用时，会导致字符在使用时彼此放在前面 `text=`

* `\charscaley` 缩放比例与使用时不 `text=` 同，但不会影响行高。

* 如果最后一行文本不适合，则整个行将被删除，而不显示为截止。
* `\slmult` 而且 `\sl` 行为与MS Word不同 `text=`，它们只会对当前和后续段落生效。

* `\sb` 适用于MS Word和、Adobe InDesign和 `text=`Photoshop的第一段，但不适用。

* `\sa` 适用于MS Word和、Adobe InDesign和 `text=`Photoshop的最后一段。

## 向后兼容性{#section-a76842f751944f4fb664af296d064122}

* 使用RTF字符串转义下划线字符(`\_`)不能用于使用`textPs=`的所有字体

* 支持不区分大小写的宏处理。
* 目录缓存已从60秒减少到10秒。
* 错误重定向功能现在仅重定向引用已发布在目录中但未在磁盘上找到的损坏图像、字体、颜色用户档案和图像的请求。
* `posN=`、 `anchor=`、、 `anchorN=`和现在 `origin=`，如果任 `originN=` 何修饰符值大于2147483648，则返回解析错误。

* 不支持嵌套请求的编码。 过渡到新行为，并取消对您站点上和公司目录中URL请求中的任何嵌套请求值的编码。
* 现在，DefaultImage在使用`req=tmb`时应用缩略图属性。
* 在使用`flip=`的早期版本中，无论锚点是什么，都不会重新定位图像。

## 适用于第三方库{#section-79768b96bf634e44ab672c5b893f343d}的限制

如果已检测到图像，Digimarc库拒绝将Digimarc水印应用于图像。 如果对主图像进行了足够的编辑，Digimarc库可能仍能识别已应用水印。 但是，它可能无法读取该信息。 这会产生一个新图像，在该新图像中无法获得应用于原始图像的原始Digimarc信息。 图像服务现在可以应用在公司目录中定义的Digimarc水印。

## 适用于图像服务和图像渲染的限制{#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 当有超过4个CPU可用时，图像服务和图像渲染可能无法充分利用所有CPU。 在这些计算机上模拟流量，了解4个以上CPU的优势。
* 返回重定向（HTTP状态301、302或303）的远程URL被拒绝。
* 配置`errorRedirect.rootUrl`时，此属性中定义的IP地址需要包含在该服务器上的规则集`<addressfilter>`标记值中。

   *示例*:

   服务器A已定义`errorRedirect.rootUrl=10.10.10.10`。

   服务器B的IP地址为10.10.10.10，它将规则集文件中的`<addressfilter>`标记值设置为包含其IP地址(10.10.10.10)。

* 具有定位的点文本和文本路径可能显示剪切。
* `text=` 仅应用 `\sa` 和 `\sb` 于整个文本块，而不是按段落。

* 当使用在URL中定义的公司和为`src=`或`mask=`修饰符定义的其他公司时，您必须在为`src=`或`mask=`定义的公司前加正斜杠，才能使此形式的请求正常工作。

   *示例*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   而不是：`/is/image/MyCompany?src=YourCompany/MyImage`。

* 非金字塔Tiff或晕影请求会生成类似的错误消息，

   *“图 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 像没有有效的DSF，2.25MPixel的面积超过2MPixel的最大面积* 。”

   最佳做法是使用吡喃Tiff和晕影。 如果您需要使用非吡喃的tiff或晕影，请按照以下说明增加大小限制。

   *解决问题*:

   对于“图像渲染非吡唑并晕影”，请在[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]配置文件中增加IrMaxNonPyrVignetteSize的属性值。

   对于“图像服务”非吡唑化TIFF，请在[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]配置文件中增加`MaxNonDsfSize`的属性值。

* Adobe Photoshop CS3默认情况下不存储复合图像的分层PSD文件。

   *症状*:

   Adobe Photoshop CS3分层PSD文件显示为黑色，并且文本中写有“此分层Photoshop文件未与合成图像一起保存。” 用于“图像服务”回复图像或IPS。

   *解決辦法*︰

   打开最大兼容性时保存Adobe Photoshop CS3文件。

* 将ICC用户档案指定给CMYK/JPEG回复图像会导致某些浏览器中的颜色发生反转。*解决问题*:

   使用`fmt=`更改回复图像格式

* 压缩后HTTP响应图像数据（包括文件头）的大小限制为16 MB。
* &quot; .&quot; 不允许在HTTP请求中的任何路径元素中使用。
* 卸载可从&#x200B;*[!DNL install_root]*&#x200B;或任何子文件夹删除用户创建或修改的文件。 卸载前将这些文件复制到其他位置。

## 仅适用于图像服务{#section-b08ad535e4454265b8157dec244c4faf}的限制

* PhotoFont文本不支持RTF(`\cf`)命令中的前景色。
* 合成粗体、斜体和粗体/斜体将作为PhotoFont文本的错误被拒绝。
* PhotoFont文本不支持垂直文本排列。
* PhotoFont文本不支持16bpc PNG图像。
* 具有嵌入颜色用户档案的PNG图像的颜色校正使用硬编码选项。 渲染方法为相对比色，并且PhotoFont文本的黑点补偿处于打开状态。
* 在公司 [!DNL ini]文件中启用区域设置转换时，不支持基于文件的查找。
* 图像服务无法正确写入非闭合Photoshop路径。
* 图像服务当前不支持处理使用Adobe Media Encoder 4.0.1或更早版本导出的TIFF文件。 Adobe Media Encoder包含在Premiere Pro CS4、After Effects CS4和Creative Suite 4 Production Premium中。
* 对自调整图层使用`text=`不支持使用多个设置进行行对齐的RTF字符串。

   *示例*

   RTF字符串不能对自调整大小的文本图层同时使用左行和右行对齐。

* SVG对于未嵌入SVG文件的引用字体的字体查找路径具有其自己的属性。

   *症状*

   呈现的包含字体定义的SVG图像使用的字体不正确。

   *解决方法*

   在[!DNL install_root/ImageServing/conf/PlatformServer.conf]中设置属性`svgProvider.fontRoot=`。

* 裁剪当前使用`bgColor=`代替`color=`来填充任何新扩展区域。

* 当`bgColor=`与涉及颜色用户档案的基色空间不匹配时，颜色转换可能不正确。
* 如果图层没有蒙版或Alpha数据，则不渲染外层效果。

## 仅适用于图像渲染{#section-4c6949e797174607a3d1ab4d3d4a725a}的限制

* 墙体和墙体材料无法拆卸。
* 纹理的大小相对于晕影视图的大小有限。 在极少数情况下，默认限制为视图大小的425%可能会干扰使用超大非可重复纹理的应用程序。 如果无法将应用程序或内容更改为在预定义的限制范围内工作，则百分比可以增加如下。 使用文本编辑器，打开[!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]，找到`IrMaxTextureSizeFactor`并输入新的百分比值。 更改将立即生效，无需重新启动图像服务器。

* Netscape和Opera中的JavaScript引擎缓存响应数据，即使已设置nocache头。 这妨碍了有国家要求的正常运作。

   *解决方法*

   在请求字符串中附加时间戳或其他唯一标识符，如`"&.ts=currentTime`。

## 仅适用于实用程序{#section-906a6b2378154b3da122b2332983f7a5}的限制

`ImageConvert`有时，当停止时会因分段错误而崩溃 `control-c`。
