---
title: init
description: 混合媒体查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4fb40cec-172a-41b3-98fc-927da88c7cb9
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# init{#init}

混合媒体查看器的JavaScript API引用。

`init()`

启动混合媒体查看器的初始化。 此时，必须创建容器DOM元素，以便查看器代码可以通过其ID找到它。

如果容器元素尚未包含在网页布局中 — 例如，可能会使用 `display:none` style — 查看器会暂停其初始化过程。 它将一直挂起，直到网页将容器元素引回布局时为止，此时查看器加载会自动恢复。

在查看器生命周期内，只调用一次此方法；将忽略后续调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
