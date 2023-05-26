---
title: 命令引用 — 配置属性
description: 旋转查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

旋转查看器的配置属性文档。

任何配置命令都可以在URL中设置或使用 `setParam()`，或 `setParams()`或API方法二者。 任何配置属性也可以在服务器端配置记录中指定。

某些配置命令可能会带有相应Viewer SDK组件的类名称或实例名称前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` api方法。 文档包含此类命令的可选前缀。 例如， `zoomstep` 命令记录如下：

`[SpinView.|<containerId>_spinView].zoomstep`

这意味着您可以按如下方式使用此命令

* `zoomstep` （简短语法）
* `SpinView.zoomstep` （用组件类名限定）
* `cont_spinView.zoomstep` (用组件ID限定，假定 `cont` 是容器元素的ID)

另请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
