---
description: 在URL或目录修饰符命令序列中，图层定义序列用layer=命令开始，并用另一个layer=命令、effect=命令或URL末尾终止。
seo-description: 在URL或目录修饰符命令序列中，图层定义序列用layer=命令开始，并用另一个layer=命令、effect=命令或URL末尾终止。
seo-title: 指定图层
solution: Experience Manager
title: 指定图层
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 86ece2a6-5b91-4a24-baaa-542d9ae1e544
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# 指定层{#specifying-layers}

在URL或目录：:Modifier命令序列中，图层定义序列用layer=命令开始，用另一个layer=命令、effect=命令或URL末尾终止。

层定义序列中的所有命令都与层相关联。

`layer=`命令指定一个图层编号，该编号必须是整数0或更大。 具有相同图层编号的图层定义序列中的所有命令都应用于同一图层。 如果同一命令多次出现，则以最后一个实例为准。
