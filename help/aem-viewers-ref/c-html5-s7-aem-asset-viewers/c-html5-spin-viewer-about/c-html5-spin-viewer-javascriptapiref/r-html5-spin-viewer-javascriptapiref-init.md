---
description: Spin Viewer的JavaScript API参考。
seo-description: Spin Viewer的JavaScript API参考。
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

Spin Viewer的JavaScript API参考。

`init()`

开始旋转查看器的初始化。 此时，必须创 `DOM` 建容器元素，以便查看器代码能够按其ID找到它。

如果容器元素尚不是网页布局的一部分（例如，它可能使用分配给它的样式隐藏），则查看器将暂停其初始化过程，直到网页将容器元素返回到布局为止。 `display:none` 发生这种情况时，查看器加载会自动恢复。

在查看器生命周期中只调用此方法一次；随后的调用将被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

