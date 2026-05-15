---
description: 管理页面标签
solution: Experience Manager
title: 管理页面标签
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
TQID: 'https://experienceleague.adobe.com/EprHC1GFDB5Lkytg4NZf8Am0myr-jXC2wxxcefelvc8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 0%

---

# 管理页面标签{#managing-page-labels}

查看器用户界面中有两个位置显示页面标签：缩略图模式和目录下拉列表。

可以定义三种类型的标签：

* 作者使用SYMBOL本地化机制定义的标签。
* 作者在Dynamic Media Classic的后端定义的标签。
* 查看器自动生成的标签。

使用`MediaSet.LABEL_XX[_YY]`和`MediaSet.LABEL_DELIM` SYMBOL定义基于符号的标签，如[用户界面元素的本地化](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)中所述。 您可以为整个ecatalog跨页定义此类标签，在这种情况下，您应使用短的SYMBOL语法( `MediaSet.LABEL_XX`)。 或者，使用完整的SYMBOL语法( `MediaSet.LABEL_XX_YY`)为每个页面分别指定它。

当您为ecatalog跨页中的两个页面定义标签时，查看器使用`MediaSet.LABEL_DELIM` SYMBOL将这些标签串连到一个字符串中。 基于符号的标签优先于在后端定义的标签或由查看器自动生成的标签。

在Dynamic Media Classic中定义的标签存储在各个页面图像的UserData记录中。 与基于SYMBOL的标签相同。 也就是说，如果ecatalog跨页中的两个页面都定义了标签，则它们将在横向模式下使用`MediaSet.LABEL_DELIM` SYMBOL进行连接。 Dynamic Media Classic标签优先于自动生成的标签，但会被基于SYMBOL的标签覆盖。

自动生成的标签是分配给eCatalog中所有页面的序列号。 如果为给定的跨页定义了基于SYMBOL的标签或定义了Dynamic Media Classic标签，则会忽略自动生成的标签。

在目录中，可以使用`showdefault`参数禁用自动生成标签的显示。
