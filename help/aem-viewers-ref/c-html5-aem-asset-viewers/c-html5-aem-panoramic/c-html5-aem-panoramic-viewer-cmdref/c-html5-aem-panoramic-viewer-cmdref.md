---
title: 命令引用 — 配置属性
description: 全景查看器的配置属性文档。
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

全景查看器的配置属性文档。

任何配置命令都可以在URL中或使用`setParam()`和/或`setParams()` API方法进行设置。 任何配置属性也可以在服务器端配置记录中指定。

某些配置命令可能会带有相应HTML5 SDK组件的类名称或实例名称前缀。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如，`vrrender`命令记录如下：

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

这意味着，以下列方式使用此命令：

* `vrrender` （短语法）
* `PanoramicView.vrrender` （用组件类名限定）
* `cont_panoramicView.vrrender` （用组件ID限定，假设cont是容器元素的ID）


查看所有查看者通用的[命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

查看所有查看者通用的[命令引用 — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
