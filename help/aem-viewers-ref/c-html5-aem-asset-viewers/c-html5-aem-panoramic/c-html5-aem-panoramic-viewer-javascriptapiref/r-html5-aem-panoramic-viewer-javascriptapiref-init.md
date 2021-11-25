---
title: init
description: 全景查看器的JavaScript API引用。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# init{#init}

全景查看器的JavaScript API引用。

`init()`

开始初始化全景查看器。 此时，必须创建容器DOM元素，以便查看器代码可以通过其ID找到它。

如果容器元素尚未包含在网页布局中(例如，可能会使用 `display:none` 样式)，查看器将暂停其初始化过程。 直到网页将容器元素引回布局为止。 发生此事件时，查看器加载会自动恢复。

在查看器生命周期中，此方法只应调用一次，后续调用将被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
