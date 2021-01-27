---
description: 管理页面标签
solution: Experience Manager
title: 管理页面标签
topic: Dynamic Media
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# 管理页面标签{#managing-page-labels}

查看器用户界面中有两个位置显示页面标签：缩览图模式和目录下拉框。

可以定义三种类型的标签：

* 作者使用SYMBOL本地化机制定义的标签。
* 作者在后端、Scene7出版系统中定义的标签。
* 查看器自动生成的标签。

基于符号的标签使用`MediaSet.LABEL_XX[_YY]`和`MediaSet.LABEL_DELIM` SYMBOL定义，如用户界面元素](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)本地化中所述。 [您可以为整个电子目录跨页定义此类标签，在这种情况下，应使用短的SYMBOL语法(`MediaSet.LABEL_XX`)。 或者，使用完整的SYMBOL语法(`MediaSet.LABEL_XX_YY`)为每页单独指定它。

在电子目录跨页中为两个页面定义标签时，查看器使用`MediaSet.LABEL_DELIM` SYMBOL将这些标签连接到一个字符串。 基于符号的标签优先于在后端定义或查看器自动生成的标签。

在Scene7出版系统中定义的标签存储在单个页面图像的UserData记录中。 与基于SYMBOL的标签相同。 也就是说，如果电子目录跨页中的两个页面都定义了标签，则在横向模式下使用`MediaSet.LABEL_DELIM` SYMBOL连接这些页面。 Scene7出版系统标签优先于自动生成的标签，但由基于SYMBOL的标签覆盖。

自动生成的标签是分配给电子目录中所有页面的顺序编号。 如果给定跨页定义了基于SYMBOL的标签或定义了Scene7出版系统标签，则将忽略该跨页自动生成的标签。

在目录中，可以使用`showdefault`参数禁用自动生成标签的显示。
