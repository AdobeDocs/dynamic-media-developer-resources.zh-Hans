---
title: init
description: eCatalog查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4d71062c-fee7-4339-bd7f-1b7f778465c4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# init{#init}

eCatalog查看器的JavaScript API参考。

[!DNL `init()`]

启动eCatalog查看器的初始化。 到那时，必须创建容器DOM元素，以便查看器代码可以按其ID找到它。

如果容器元素还不是网页布局的一部分（例如，它可能是使用分配给它的[!DNL `display:none`]样式隐藏的），则查看器将暂停其初始化过程。 一直到网页将容器元素重新放置到布局时为止。 发生此事件时，查看器加载会自动恢复。

在查看器生命周期内仅调用一次此方法；将忽略后续调用。

## 参数 {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

无。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

[!DNL `{Object}`]对查看器实例的引用。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
