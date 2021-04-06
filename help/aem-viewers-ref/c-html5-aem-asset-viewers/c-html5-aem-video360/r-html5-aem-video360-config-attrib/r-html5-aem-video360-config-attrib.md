---
description: Video360查看器的配置属性文档。
solution: Experience Manager
title: 命令参考 — 配置属性
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

Video360查看器的配置属性文档。

可以在URL中或使用`setParam()`或`setParams()`（或同时使用两种API方法）设置任何配置命令。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令的前缀可能是相应Viewer SDK组件的类名或实例名。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档中包括此类命令的可选前缀。 例如，`playback`命令说明如下：

`[VideoPlayer.|<containerId>_videoPlayer].playback`

这意味着您可以将此命令用作：

* `playback` （短语法）
* `VideoPlayer.playback` （限定为组件类名称）
* `cont_videoPlayer.playback` (用组件ID限定，假 `cont` 定是容器元素的ID)

另请参阅[所有查看器通用的命令参考 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
