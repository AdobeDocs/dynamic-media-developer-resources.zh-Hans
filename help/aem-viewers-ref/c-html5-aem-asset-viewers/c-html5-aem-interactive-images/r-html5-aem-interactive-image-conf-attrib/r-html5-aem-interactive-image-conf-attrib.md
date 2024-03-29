---
title: 命令引用 — 配置属性
description: 交互式图像查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

交互式图像查看器的配置属性文档。

任何配置命令都可以在URL中设置或使用 `setParam()`，或 `setParams()`或API方法。 任何配置属性也可以在服务器端配置记录中指定。

某些配置命令可能会带有相应Viewer SDK组件的类名称或实例名称前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` API方法。 文档包含此类命令的可选前缀。 例如， `zoomstep` 命令记录如下：

`[ZoomView.|<containerId>_zoomView].fmt`

这意味着您可以将此命令用作：

* `fmt` （简短语法）
* `ZoomView.fmt` （用组件类名限定）
* `cont_zoomView.fmt` (使用组件ID限定，假定 `cont` 是容器元素的ID)

另请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
