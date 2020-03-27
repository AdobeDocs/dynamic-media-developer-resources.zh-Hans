---
description: 弹出查看器的配置属性文档
seo-description: 弹出查看器的配置属性文档
seo-title: 命令参考——配置属性
solution: Experience Manager
title: 命令参考——配置属性
topic: Dynamic media
uuid: 0813c334-37b7-43af-b39d-bec66658ad58
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 命令参考——配置属性{#command-reference-configuration-attributes}

弹出查看器的配置属性文档

您可以在URL中设置任何配置命令。 或者，您可以使 `setParam()`用、 `setParams()`或同时使用两种API方法。 您还可以在服务器端配置记录中指定任何配置属性。

某些配置命令的前缀为相应查看器SDK组件的类名或实例名。 组件的实例名称是动态的，并取决于传递给 `setContainerId()` API方法的查看器容器DOM元素的ID。 文档中包含此类命令的可选前缀。 例如，命令 `zoomfactor` 的说明如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

该命令的用法如下：

* `zoomfactor` （短语法）
* `FlyoutZoomView.zoomfactor` （用组件类名称限定）
* `cont_flyout.zoomfactor` (用组件ID限定，假定 `cont` 它是容器元素的ID)

另请参阅所 [有查看器通用的命令参考——配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
