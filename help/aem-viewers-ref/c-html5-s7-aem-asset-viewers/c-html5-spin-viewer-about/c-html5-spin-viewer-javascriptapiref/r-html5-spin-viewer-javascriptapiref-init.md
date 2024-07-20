---
title: init
description: 旋转查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# init{#init}

旋转查看器的JavaScript API参考。

`init()`

启动旋转查看器的初始化。 此时必须创建容器`DOM`元素，以便查看器代码可以按其ID找到它。

如果容器元素还不是网页布局的一部分（例如，它可能使用`display:none`样式隐藏），则查看器将暂停其初始化过程。 该面板将暂停，直到网页将容器元素重新添加到布局时，查看器加载会自动恢复。

在查看器生命周期内仅调用一次此方法；将忽略后续调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
