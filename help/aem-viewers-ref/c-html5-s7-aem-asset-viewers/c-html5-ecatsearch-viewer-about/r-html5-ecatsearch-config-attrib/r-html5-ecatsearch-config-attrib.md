---
description: eCatalog查看器的配置属性文档。
solution: Experience Manager
title: 命令引用 — 配置属性
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

eCatalog查看器的配置属性文档。

任何配置命令都可以在URL中设置，也可以使用`setParam()`或`setParams()`（或同时使用两者）API方法进行设置。 您还可以指定在服务器端配置记录中指定的任何配置属性。

对于某些配置命令，您可以为它们添加前缀，使用相应查看器SDK组件的类名或实例名。 组件的实例名称是动态的，具体取决于传递到`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如， `zoomstep`命令记录如下：

`[PageView.|<containerId>_pageView].zoomstep`

这表示您可以将此命令用作：

* `zoomstep` （短语法）
* `PageView.zoomstep` （使用组件类名称限定）
* `cont_pageView.zoomstep` (使用组件ID进行鉴别， `cont` 假定是容器元素的ID)

另请参阅[所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
