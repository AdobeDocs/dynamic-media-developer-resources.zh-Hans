---
title: 管理页面标签
description: 管理页面标签
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 管理页面标签{#managing-page-labels}

查看器用户界面中有两个位置显示页面标签：缩略图模式和目录下拉列表。

可以定义三种类型的标签：

* 作者使用SYMBOL本地化机制定义的标签。
* 作者在Dynamic Media Classic内的后端定义的标签。
* 查看器自动生成的标签。

基于符号的标签是使用 `MediaSet.LABEL_XX[_YY]` 和 `MediaSet.LABEL_DELIM` 符号(如 [用户界面元素的本地化](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). 您可以为整个ecatalog跨页定义此类标签，在这种情况下，应使用短的SYMBOL语法( `MediaSet.LABEL_XX`)。 或者，使用完整的SYMBOL语法( `MediaSet.LABEL_XX_YY`)。

在ecatalog跨页中为两个页面定义标签时，查看器会使用 `MediaSet.LABEL_DELIM` 符号。 基于符号的标签优先于在后端定义的标签或查看器自动生成的标签。

在Dynamic Media Classic中定义的标签存储在单个页面图像的UserData记录中。 与基于符号的标签相同。 也就是说，如果ecatalog扩展中的两个页面都定义了标签，则会使用 `MediaSet.LABEL_DELIM` 横向模式下的符号。 Dynamic Media Classic标签优先于自动生成的标签，但会被基于SYMBOL的标签覆盖。

自动生成的标签是分配给ecatalog中所有页面的顺序编号。 如果给定的跨页定义了基于符号的标签或定义了Dynamic Media Classic标签，则会忽略该跨页自动生成的标签。

在目录中，可以使用 `showdefault` 参数。
