---
description: eCatalog查看器的配置属性文档。
solution: Experience Manager
title: 命令引用 — 配置属性
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

eCatalog查看器的配置属性文档。

任何配置命令都可以在URL中设置，或者使用`setParam()`、`setParams()`或API方法同时设置。 您还可以指定在服务器端配置记录中指定的任何配置属性。

对于某些配置命令，您可以使用相应Viewer SDK组件的类名称或实例名称作为前缀。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如，`zoomstep`命令记录如下：

`[PageView.|<containerId>_pageView].zoomstep`

这意味着您可以将此命令用作：

* `zoomstep` （短语法）
* `PageView.zoomstep` （用组件类名限定）
* `cont_pageView.zoomstep` （用组件ID限定，假设`cont`是容器元素的ID）

另请参阅[所有查看者通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
