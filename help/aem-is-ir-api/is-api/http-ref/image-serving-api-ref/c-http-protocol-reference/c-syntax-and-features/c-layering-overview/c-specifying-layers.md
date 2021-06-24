---
description: 在URL或目录修饰符命令序列中，层定义序列以layer=命令开头，并以另一个layer=命令、effect=命令或URL结尾终止。
solution: Experience Manager
title: 指定图层
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# 指定图层{#specifying-layers}

在URL或目录：:Modifier命令序列中，层定义序列以layer=命令开头，以另一个layer=命令、effect=命令或URL的结尾终止。

层定义序列中的所有命令都与层相关联。

`layer=`命令指定一个层数，该层数必须是0或更大的整数。 具有相同层编号的层定义序列中的所有命令都应用于同一层。 如果同一命令多次发生，则最后一个实例将占上风。
