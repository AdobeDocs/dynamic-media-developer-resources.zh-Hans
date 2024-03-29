---
title: 命令引用 — 配置属性
description: eCatalog查看器的配置属性文档。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

eCatalog查看器的配置属性文档。

任何配置命令都可以在URL中设置或使用 `setParam()`，或 `setParams()`或API方法二者。 您还可以指定在服务器端配置记录中指定的任何配置属性。

对于某些配置命令，可以使用相应查看器SDK组件的类名或实例名作为前缀。 组件的实例名称是动态的，具体取决于传递给的查看器容器DOM元素的ID `setContainerId()` api方法。 文档包含此类命令的可选前缀。 例如， `zoomstep` 命令记录如下：

`[PageView.|<containerId>_pageView].zoomstep`

这意味着您可以将此命令用作

* `zoomstep` （简短语法）
* `PageView.zoomstep` （用组件类名限定）
* `cont_pageView.zoomstep` (用组件ID限定，假定 `cont` 是容器元素的ID)

另请参阅 [所有查看器通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
