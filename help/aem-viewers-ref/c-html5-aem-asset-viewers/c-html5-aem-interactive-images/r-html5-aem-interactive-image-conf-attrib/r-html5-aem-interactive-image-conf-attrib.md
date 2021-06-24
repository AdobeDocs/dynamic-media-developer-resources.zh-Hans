---
description: 交互式图像查看器的配置属性文档。
solution: Experience Manager
title: 命令引用 — 配置属性
feature: Dynamic Media Classic，查看器，SDK/API，交互式图像
role: Developer,Business Practitioner
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

交互式图像查看器的配置属性文档。

任何配置命令都可以在URL中设置，也可以使用`setParam()`或`setParams()`（或同时使用两者）API方法进行设置。 也可以在服务器端配置记录中指定任何配置属性。

某些配置命令可能带有相应查看器SDK组件的类名或实例名的前缀。 组件的实例名称是动态的，具体取决于传递到`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如， `zoomstep`命令记录如下：

`[ZoomView.|<containerId>_zoomView].fmt`

这表示您可以将此命令用作：

* `fmt` （短语法）
* `ZoomView.fmt` （使用组件类名称限定）
* `cont_zoomView.fmt` (使用组件ID进行鉴别， `cont` 假定是容器元素的ID)

另请参阅[所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
