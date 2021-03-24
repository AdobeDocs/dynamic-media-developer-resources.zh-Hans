---
description: 在URL或目录修饰符命令序列中，图层定义序列开始使用layer=命令，并用另一个layer=命令、effect=命令或URL的结尾终止。
solution: Experience Manager
title: 指定图层
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# 指定图层{#specifying-layers}

在URL或目录：:Modifier命令序列中，图层定义序列开始使用layer=命令，并用另一个layer=命令、effect=命令或URL的结尾终止。

图层定义序列中的所有命令都与图层关联。

`layer=`命令指定一个图层编号，该编号必须是整数0或更大。 具有相同图层编号的图层定义序列中的所有命令都将应用于同一图层。 如果同一命令多次发生，则最后一个实例将优先。
