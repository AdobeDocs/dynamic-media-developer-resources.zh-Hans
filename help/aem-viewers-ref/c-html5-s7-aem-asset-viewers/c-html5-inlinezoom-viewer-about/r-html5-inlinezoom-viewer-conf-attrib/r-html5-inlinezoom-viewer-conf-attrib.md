---
title: 命令引用 — 配置属性
description: 弹出查看器的配置属性文档
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

弹出查看器的配置属性文档

您可以在URL中设置任何配置命令。 或者，您可以使用 `setParam()`, `setParams()`，或两种API方法。 您还可以在服务器端配置记录中指定任何配置属性。

某些配置命令带有类名或相应查看器SDK组件的实例名的前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` API方法。 文档包含此类命令的可选前缀。 例如， `zoomfactor` 命令的说明如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

该命令的使用如下所示：

* `zoomfactor` （短语法）
* `FlyoutZoomView.zoomfactor` （使用组件类名称进行限定）
* `cont_flyout.zoomfactor` (使用组件ID进行鉴别，假定 `cont` 是容器元素的ID)

另请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
