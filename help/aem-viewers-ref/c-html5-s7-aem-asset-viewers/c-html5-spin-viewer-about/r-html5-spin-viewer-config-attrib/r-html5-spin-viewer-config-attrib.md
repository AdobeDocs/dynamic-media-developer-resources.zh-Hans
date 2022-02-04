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

可以在URL中或使用 `setParam()`或 `setParams()`，或两者都是API方法。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令可能带有相应查看器SDK组件的类名或实例名的前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` API方法。 文档包含此类命令的可选前缀。 例如， `zoomstep` 命令的说明如下：

`[SpinView.|<containerId>_spinView].zoomstep`

这表示您可以按如下方式使用此命令

* `zoomstep` （短语法）
* `SpinView.zoomstep` （使用组件类名称限定）
* `cont_spinView.zoomstep` (使用组件ID进行鉴别，假定 `cont` 是容器元素的ID)

另请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
