---
description: 缩放查看器的配置属性文档。
seo-description: 缩放查看器的配置属性文档。
seo-title: 命令参考 — 配置属性
solution: Experience Manager
title: 命令参考 — 配置属性
uuid: 1bcc879a-12ec-4924-ac05-2e4c1d6e4597
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# 命令引用 — 配置属性{#command-reference-configuration-attributes}

缩放查看器的配置属性文档。

可以在URL中或使用`setParam()`或`setParams()`（或同时使用两种API方法）设置任何配置命令。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令的前缀可能是相应Viewer SDK组件的类名或实例名。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档中包括此类命令的可选前缀。 例如，`zoomstep`命令说明如下：

`[ZoomView.|<containerId>_zoomView].zoomstep`

这意味着您可以将此命令用作：

* `zoomstep` （短语法）
* `ZoomView.zoomstep` （限定为组件类名称）
* `cont_zoomView.zoomstep` (用组件ID限定，假 `cont` 定是容器元素的ID)

另请参阅[所有查看器通用的命令参考 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
