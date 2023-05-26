---
description: eCatalog查看器的JavaScript API参考。
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# init{#init}

eCatalog查看器的JavaScript API参考。

[!DNL `init()`]

启动eCatalog查看器的初始化。 此时，必须创建容器DOM元素，以便查看器代码可以按其ID找到它。

如果容器元素还不是网页布局的一部分(例如，它可能使用以下项目隐藏： [!DNL `display:none`] 样式)，查看器会暂停其初始化过程，直到网页将容器元素重新调整到布局为止。 发生这种情况时，查看器加载会自动恢复。

在查看器生命周期内只调用一次此方法；后续调用将被忽略。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`] 对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
