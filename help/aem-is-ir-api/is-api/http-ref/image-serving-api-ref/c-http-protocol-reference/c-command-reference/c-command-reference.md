---
description: 本节介绍HTTP协议命令。
solution: Experience Manager
title: 命令参考
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 10%

---


# 命令引用{#command-reference}

本节介绍HTTP协议命令。

**仅适用于AEM中的Dynamic Media**:除了用户界面中提供的基本图像设置，AEM()中 [!DNL Dynamic Media] 还支 [!DNL Adobe Experience Manager]持在“图像修改”中指定的大量高级 **图像** 修改。这些参数定义如下。 但是，请注意，AEM中的Dynamic Media不支持以下功能。

* 颜色校正命令：`icc=`和`iccEmbed=`。
* 基本模板和文本渲染命令：`text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=`和`textPs=`。
* 本地化命令：`locale=`和`req=xlate`。
* `req=set` 不可用于一般用途。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 非核心Dynamic Media服务：SVG、图像渲染和Web到打印。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

另请参阅AEM 6.5文档中的Dynamic Media [图像预设选项](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic)。

* [对齐](r-align.md)
* [锚记](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [缓存](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [裁切](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [效果](r-effect.md)
* [effectMask](r-effectmask.md)
* [扩展](r-extend.md)
* [适合](r-fit.md)
* [翻转](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [隐藏](r-hide.md)
* [ic](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [图层](r-layer.md)
* [locale](r-locale.md)
* [地图](r-map.md)
* [蒙版](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_growMask](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
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
* [数量](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotate](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [大小](r-size-reference.md)
* [src](r-src.md)
* [模板](r-template.md)
* [文字](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [类型](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
