---
description: 内联缩放查看器的JavaScript API参考。
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 2%

---


# init{#init}

内联缩放查看器的JavaScript API参考。

`init()`

开始查看器的初始化，以便查看器代码可以按其ID找到它。 此时必须创建容器 DOM元素。

如果容器元素尚不是网页布局的一部分（例如，它可能使用分配给它的`display:none`样式被隐藏），则查看器将暂停其初始化过程，直到网页将容器元素返回到布局为止。 发生这种情况时，查看器加载会自动恢复。

在查看器生命周期中，只调用一次此方法；将忽略后续调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回{#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

