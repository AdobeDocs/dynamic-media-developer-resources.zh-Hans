---
description: 'null'
seo-description: 'null'
seo-title: 管理页面标签
solution: Experience Manager
title: 管理页面标签
topic: Dynamic media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 管理页面标签{#managing-page-labels}

查看器用户界面中有两个位置显示页面标签：缩览图模式和目录下拉列表。

可以定义三种类型的标签：

* 作者使用SYMBOL本地化机制定义的标签。
* 作者在后端SPS中定义的标签。
* 查看器自动生成的标签。

基于符号的标签是使用SYMBOL `MediaSet.LABEL_XX[_YY]` 和 `MediaSet.LABEL_DELIM` SYMBOL定义的，如用 [户界面元素本地化中所述](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。 您可以为整个电子目录跨页定义此类标签，在这种情况下，应使用短的SYMBOL语法( `MediaSet.LABEL_XX`)。 或者，使用完整的SYMBOL语法( `MediaSet.LABEL_XX_YY`)为每页单独指定它。

当您为电子目录跨页中的两个页面定义标签时，查看器使用 `MediaSet.LABEL_DELIM` SYMBOL将这些标签连接为一个字符串。 基于符号的标签优先于在后端定义或查看器自动生成的标签。

在SPS中定义的标签存储在单个页面图像的用户数据记录中。 与基于SYMBOL的标签相同。 也就是说，如果电子目录跨页中的两个页面都定义了标签，则它们会在横向模式下使用 `MediaSet.LABEL_DELIM` SYMBOL连接。 SPS标签优先于自动生成的标签，但由基于SYMBOL的标签覆盖。

自动生成的标签是分配给目录中所有页面的顺序编号。 如果给定跨页定义了基于符号的标签或定义了SPS标签，则会忽略自动生成的标签。

在目录中，可以使用参数禁用自动生成的标签的显 `showdefault` 示。
