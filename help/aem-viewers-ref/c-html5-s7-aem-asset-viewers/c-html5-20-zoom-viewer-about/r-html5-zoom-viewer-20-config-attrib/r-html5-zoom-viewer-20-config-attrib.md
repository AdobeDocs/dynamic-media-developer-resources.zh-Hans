---
title: 命令引用 — 配置属性
description: 缩放查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

缩放查看器的配置属性文档。

可以在URL中或使用 `setParam()`或 `setParams()`，或两者都是API方法。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令可能带有相应查看器SDK组件的类名或实例名的前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` API方法。 文档包含此类命令的可选前缀。 例如， `zoomstep` 命令的说明如下：

`[ZoomView.|<containerId>_zoomView].zoomstep`

这表示您可以将命令用作

* `zoomstep` （短语法）
* `ZoomView.zoomstep` （使用组件类名称限定）
* `cont_zoomView.zoomstep` (使用组件ID进行鉴别，假定 `cont` 是容器元素的ID)

另请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
