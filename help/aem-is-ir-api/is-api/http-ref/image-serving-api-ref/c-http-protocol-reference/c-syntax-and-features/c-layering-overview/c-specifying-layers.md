---
description: 在URL或catalog Modifier命令序列中，层定义序列以layer=命令开头，以另一个layer=命令、effect=命令或URL的结尾结尾。
solution: Experience Manager
title: 指定层
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# 指定层{#specifying-layers}

在URL或catalog：：Modifier命令序列中，图层定义序列以layer=命令开头，以另一个layer=命令、effect=命令或URL结尾结尾。

图层定义序列中的所有命令都与图层相关联。

此 `layer=` command指定图层编号，它必须是大于或等于0的整数。 图层定义序列中具有相同图层编号的所有命令都应用于同一图层。 如果同一命令多次出现，则最后一个实例将占上风。
