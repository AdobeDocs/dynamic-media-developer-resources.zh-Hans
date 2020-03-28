---
description: 传送查看器的配置属性文档。
seo-description: 传送查看器的配置属性文档。
seo-title: 命令参考——配置属性
solution: Experience Manager
title: 命令参考——配置属性
topic: Dynamic media
uuid: 036af728-ab00-4db3-98cf-d16f1bffa064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 命令参考——配置属性{#command-reference-configuration-attributes}

传送查看器的配置属性文档。

可以在URL中设置任何配置命令，也可以使 `setParam()`用API方 `setParams()`法或／或两者设置。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令的前缀可能是相应查看器SDK组件的类名或实例名。 组件的实例名称是动态的，并取决于传递给 `setContainerId()` API方法的查看器容器DOM元素的ID。 文档中包含此类命令的可选前缀。 例如，命 `zoomstep` 令的说明如下：

`[ZoomView.|<containerId>_carouselView].fmt`

这意味着您可以将此命令用作：

* `fmt` （短语法）
* `CarouselView.fmt` （用组件类名称限定）
* `cont_carouselView.fmt` (用组件ID限定，假 `cont` 定是容器元素的ID)

另请参阅所 [有查看器通用的命令参考——配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
