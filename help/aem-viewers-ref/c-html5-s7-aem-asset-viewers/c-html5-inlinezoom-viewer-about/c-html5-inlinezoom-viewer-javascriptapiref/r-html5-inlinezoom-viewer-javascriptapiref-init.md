---
description: 内联缩放查看器的JavaScript API引用。
solution: Experience Manager
title: init
feature: Dynamic Media Classic，查看器，SDK/API，内联缩放
role: Developer,Business Practitioner
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

内联缩放查看器的JavaScript API引用。

`init()`

启动查看器的初始化，以便查看器代码可以按其ID查找。 此时必须创建容器DOM元素。

如果容器元素尚未成为网页布局的一部分（例如，可能使用分配给它的`display:none`样式来隐藏该元素），查看器会暂停其初始化过程，直到网页将容器元素返回到布局为止。 发生此情况时，查看器加载会自动恢复。

在查看器生命周期内，只调用一次此方法；将忽略后续调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
