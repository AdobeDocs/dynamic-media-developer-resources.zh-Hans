---
description: 弹出查看器的配置属性文档
seo-description: 弹出查看器的配置属性文档
seo-title: 命令参考 — 配置属性
solution: Experience Manager
title: 命令参考 — 配置属性
uuid: d7e89a24-a235-4f20-86d1-25aacd118880
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# 命令引用 — 配置属性{#command-reference-configuration-attributes}

弹出查看器的配置属性文档

可以在URL中设置任何配置命令。 或者，可以使用`setParam()`、`setParams()`或两种API方法。 您还可以在服务器端配置记录中指定任何配置属性。

某些配置命令的前缀为类名或相应查看器SDK组件的实例名。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档中包括此类命令的可选前缀。 例如，`zoomfactor`命令说明如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

命令的用法如下：

* `zoomfactor` （短语法）
* `FlyoutZoomView.zoomfactor` （用组件类名称限定）
* `cont_flyout.zoomfactor` (使用组件ID限定，假 `cont` 定该ID是容器元素的ID)

另请参阅[所有查看器通用的命令参考 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
