---
title: 命令引用 — 配置属性
description: 弹出查看器的配置属性文档
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
TQID: 'https://experienceleague.adobe.com/Bus1MH5Y8xppGXxnARx0Fq11dslSbY9Q7yAlFtF6KzI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 0%

---

# 命令引用 — 配置属性{#command-reference-configuration-attributes}

弹出查看器的配置属性文档

您可以在URL中设置任何配置命令。 或者，您可以使用`setParam()`、`setParams()`或这两种API方法。 您还可以在服务器端配置记录中指定任何配置属性。

某些配置命令带有相应查看器SDK组件的类名或实例名前缀。 组件的实例名称是动态的，取决于传递给`setContainerId()` API方法的查看器容器DOM元素的ID。 文档包含此类命令的可选前缀。 例如，`zoomfactor`命令记录如下：

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

该命令的使用方法如下：

* `zoomfactor` （短语法）
* `FlyoutZoomView.zoomfactor` （用组件类名限定）
* `cont_flyout.zoomfactor` （使用组件ID进行限定，假设`cont`是容器元素的ID）

另请参阅[所有查看者通用的命令引用 — 配置属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
