---
title: 命令引用
description: 本节介绍HTTP协议命令。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 4%

---

# 命令引用{#command-reference}

本节介绍HTTP协议命令。

>[!TIP]
>
>尝试使用Dynamic Media [_快照_](https://snapshot.scene7.com/)来发现Dynamic Media图像修饰符和智能成像的好处。
>
> Snapshot是一种可视化演示工具，旨在说明Dynamic Media在优化和动态图像投放方面的强大功能。 试验测试图像或Dynamic Media URL，以可视化方式观察各种Dynamic Media图像修饰符的输出，以及针对以下各项的智能成像优化：
>* 文件大小（使用WebP和AVIF交付）
>* 网络带宽
>* DPR（设备像素比率）
>
>要了解使用快照的容易程度，请播放[快照培训视频](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=zh-Hans)（3分17秒）。


**仅适用于Adobe Experience Manager中的Dynamic Media** — 除了用户界面中可用的基本图像设置之外，AEM中的[!DNL Dynamic Media] ([!DNL Adobe Experience Manager])还支持您可以在&#x200B;**图像修饰符**&#x200B;字段中指定的大量高级图像修改。 这些参数定义如下。 但是，请注意，AEM中的Dynamic Media不支持以下功能。

* 颜色校正命令： `icc=`和`iccEmbed=`。
* 基本模板化和文本渲染命令： `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=`和`textPs=`。
* 本地化命令： `locale=`和`req=xlate`。
* `req=set`不可用于一般用途。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 非核心Dynamic Media服务：SVG、图像渲染和Web到打印。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

另请参阅AEM 6.5文档中的Dynamic Media [图像预设选项](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html?lang=zh-Hans#dynamic)。

* [对齐](r-align.md)
* [锚记](r-anchor.md)
* [BFC](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [混合模式](r-blendmode.md)
* [缓存](r-is-http-cache.md)
* [clip路径](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [颜色](r-color-commandref.md)
* [裁切](r-crop.md)
* [裁切路径E](r-croppath.md)
* [defaultimage](r-is-http-defaultimage.md)
* [dpr](r-dpr.md)
* [效果](r-effect.md)
* [效果蒙版](r-effectmask.md)
* [扩展](r-extend.md)
* [适合](r-fit.md)
* [翻转](r-flip.md)
* [格式](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [隐藏](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [图像集](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [图层](r-layer.md)
* [区域设置](r-locale.md)
* [地图](r-map.md)
* [蒙版](r-mask.md)
* [maskUse](r-maskuse.md)
* [网络](r-network.md)
* [op_blur](r-op-blur.md)
* [op_亮度](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_growMask](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op噪声](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [来源](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [透视](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [量化](r-is-http-quantize.md)
* [矩形](r-rect.md)
* [需要](r-req/r-req.md)
* [res](r-res.md)
* [解析模式](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [旋转](r-rotate.md)
* [缩放](r-is-http-scale.md)
* [scl](r-scl.md)
* [大小](r-size-reference.md)
* [src](r-src.md)
* [模板](r-template.md)
* [文字](r-text.md)
* [文本角度](r-textangle.md)
* [textAttr](r-textattr.md)
* [文本流路径](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [文本路径](r-textpath.md)
* [textPs](r-textps.md)
* [类型](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
