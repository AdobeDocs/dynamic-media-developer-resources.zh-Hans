---
description: 交互式视频查看器的配置属性文档。
seo-description: 交互式视频查看器的配置属性文档。
seo-title: 命令参考——配置属性
solution: Experience Manager
title: 命令参考——配置属性
topic: Dynamic media
uuid: eaf7a1a2-b0ec-4df2-926b-5e2c4cd0b3d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 命令参考——配置属性{#command-reference-configuration-attributes}

交互式视频查看器的配置属性文档。

可以在URL中设置任何配置命令，也可以使 `setParam()`用API方 `setParams()`法或／或两者设置。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令的前缀可能是相应查看器SDK组件的类名或实例名。 组件的实例名称是动态的，并取决于传递给 `setContainerId()` API方法的查看器容器DOM元素的ID。 文档中包含此类命令的可选前缀。 例如，命 `playback` 令的说明如下：

`[VideoPlayer.|<containerId>_videoPlayer].playback`

这意味着您可以将此命令用作：

* `playback` （短语法）
* `VideoPlayer.playback` （用组件类名称限定）
* `cont_videoPlayer.playback` (用组件ID限定，假 `cont` 定是容器元素的ID)

另请参阅所 [有查看器通用的命令参考——配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
