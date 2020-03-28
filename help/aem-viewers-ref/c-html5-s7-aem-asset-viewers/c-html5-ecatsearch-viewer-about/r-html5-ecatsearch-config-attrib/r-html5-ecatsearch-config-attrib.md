---
description: eCatalog Viewer的配置属性文档。
seo-description: eCatalog Viewer的配置属性文档。
seo-title: 命令参考——配置属性
solution: Experience Manager
title: 命令参考——配置属性
topic: Dynamic media
uuid: e1111ce2-67e8-449a-9cc2-bb53b61158a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 命令参考——配置属性{#command-reference-configuration-attributes}

eCatalog Viewer的配置属性文档。

可以在URL中设置任何配置命令，也可以使 `setParam()`用API方 `setParams()`法或／或两者设置。 您还可以指定在服务器端配置记录中指定的任何配置属性。

对于某些配置命令，您可以在这些命令前加上相应的查看器SDK组件的类名或实例名。 组件的实例名称是动态的，并取决于传递给 `setContainerId()` API方法的查看器容器DOM元素的ID。 文档中包含此类命令的可选前缀。 例如，命 `zoomstep` 令的说明如下：

`[PageView.|<containerId>_pageView].zoomstep`

这意味着您可以将此命令用作：

* `zoomstep` （短语法）
* `PageView.zoomstep` （用组件类名称限定）
* `cont_pageView.zoomstep` (用组件ID限定，假 `cont` 定是容器元素的ID)

另请参阅所 [有查看器通用的命令参考——配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
