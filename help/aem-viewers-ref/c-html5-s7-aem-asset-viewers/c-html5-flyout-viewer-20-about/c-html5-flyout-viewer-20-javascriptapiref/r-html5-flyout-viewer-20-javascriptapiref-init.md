---
title: init
description: 用于初始化弹出查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# init{#init}

适用于弹出查看器的JavaScript API参考。

`init()`

启动弹出查看器的初始化。 此时，必须创建容器DOM元素，以便查看器代码可以按其ID找到它。

例如，如果容器元素还不是网页布局的一部分，则可以使用隐藏该元素 `display:none` 为其指定的样式 — 查看器将暂停其初始化过程。 一直到网页将容器元素重新放置到布局时为止。 发生这种情况时，查看器加载会自动恢复。

在查看器生命周期内只应调用一次此方法，随后的调用将被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
