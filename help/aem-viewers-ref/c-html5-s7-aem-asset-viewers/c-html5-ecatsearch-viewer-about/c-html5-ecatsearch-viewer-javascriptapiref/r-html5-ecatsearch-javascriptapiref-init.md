---
description: eCatalog Viewer的JavaScript API参考。
seo-description: eCatalog Viewer的JavaScript API参考。
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: b01f1497-8bee-4e01-8f92-272b324cb2dd
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# init{#init}

eCatalog Viewer的JavaScript API参考。

[!DNL `init()`]

开始eCatalog查看器的初始化。 此时，必须创建容器DOM元素，以便查看器代码能够按其ID找到它。

如果容器元素尚不是网页布局的一部分（例如，它可能使用分配给它的样式隐藏），则查看器将暂停其初始化过程，直到网页将容器元素返回到布局为止。 [!DNL `display:none`] 发生这种情况时，查看器加载会自动恢复。

在查看器生命周期中只调用此方法一次；随后的调用将被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

