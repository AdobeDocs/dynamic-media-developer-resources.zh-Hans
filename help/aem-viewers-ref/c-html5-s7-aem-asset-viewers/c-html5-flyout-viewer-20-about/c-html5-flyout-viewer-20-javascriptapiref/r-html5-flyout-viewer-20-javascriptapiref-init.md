---
description: 弹出查看器的JavaScript API引用。
solution: Experience Manager
title: init
feature: Dynamic Media Classic，查看器，SDK/API，弹出
role: Developer,User
exl-id: e86f8c0f-c130-43c5-8c3a-07c6bc49e2f7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 2%

---

# init{#init}

弹出查看器的JavaScript API引用。

`init()`

启动弹出查看器的初始化。 此时，必须创建容器DOM元素，以便查看器代码可以通过其ID找到它。

如果容器元素尚未成为网页布局的一部分（例如，可能使用分配给它的`display:none`样式来隐藏该元素），查看器会暂停其初始化过程，直到网页将容器元素返回到布局为止。 发生此情况时，查看器加载会自动恢复。

在查看器生命周期中，此方法只应调用一次，后续调用将被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
