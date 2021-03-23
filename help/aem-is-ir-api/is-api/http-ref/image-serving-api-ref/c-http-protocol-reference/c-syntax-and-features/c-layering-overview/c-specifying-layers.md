---
description: 在URL或目录修饰符命令序列中，图层定义序列开始使用layer=命令，并用另一个layer=命令、effect=命令或URL的结尾终止。
seo-description: 在URL或目录修饰符命令序列中，图层定义序列开始使用layer=命令，并用另一个layer=命令、effect=命令或URL的结尾终止。
seo-title: 指定图层
solution: Experience Manager
title: 指定图层
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# 指定图层{#specifying-layers}

在URL或目录：:Modifier命令序列中，图层定义序列开始使用layer=命令，并用另一个layer=命令、effect=命令或URL的结尾终止。

图层定义序列中的所有命令都与图层关联。

`layer=`命令指定一个图层编号，该编号必须是整数0或更大。 具有相同图层编号的图层定义序列中的所有命令都将应用于同一图层。 如果同一命令多次发生，则最后一个实例将优先。
