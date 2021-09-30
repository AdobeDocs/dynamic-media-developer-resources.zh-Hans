---
title: init
description: 交互式视频查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

交互式视频查看器的JavaScript API引用。

`init()`

启动交互式视频查看器的初始化。 此时，必须创建容器DOM元素，以便查看器代码可以通过其ID找到它。

如果容器元素尚未包含在网页布局中 — 例如，它可能会使用分配给它的`display:none`样式进行隐藏 — 查看器会暂停其初始化过程。 直到网页将容器元素引回布局为止。 发生此事件时，查看器加载会自动恢复。

在查看器生命周期内，只调用一次此方法；将忽略后续调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
