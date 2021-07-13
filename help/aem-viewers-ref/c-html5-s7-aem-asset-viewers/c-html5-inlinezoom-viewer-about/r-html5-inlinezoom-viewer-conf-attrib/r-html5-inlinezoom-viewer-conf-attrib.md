---
description: 弹出查看器的配置属性文档
solution: Experience Manager
title: 命令引用 — 配置属性
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

弹出查看器的配置属性文档

您可以在URL中设置任何配置命令。 或者，您也可以使用`setParam()`、`setParams()`，或者同时使用这两种API方法。 您还可以在服务器端配置记录中指定任何配置属性。

某些配置命令带有类名或相应查看器SDK组件的实例名的前缀。 组件的实例名称是动态的，具体取决于传递到`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如， `zoomfactor`命令记录如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

该命令的使用如下所示：

* `zoomfactor` （短语法）
* `FlyoutZoomView.zoomfactor` （使用组件类名称进行限定）
* `cont_flyout.zoomfactor` (使用组件ID进行鉴别，假 `cont` 定是容器元素的ID)

另请参阅[所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
