---
title: init
description: 内联缩放查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# init{#init}

内联缩放查看器的JavaScript API参考。

`init()`

启动查看器的初始化，以便查看器代码可以按其ID找到它。 此时，必须创建容器DOM元素。

如果容器元素还不是网页布局的一部分（例如，它可能是使用分配给它的`display:none`样式隐藏的），查看器将暂停其初始化过程。 一直到网页将容器元素重新放置到布局时为止。 执行此操作后，查看器加载将自动继续。

在查看器生命周期内仅调用一次此方法；将忽略后续调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
