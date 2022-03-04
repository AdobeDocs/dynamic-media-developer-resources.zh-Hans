---
title: 着色材料
description: 大多数材料都可以动态着色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 着色材料{#colorizing-materials}

大多数材料都可以动态着色。

着色算法简单，对于具有有限色调范围的材料图像效果最好。 要对材料进行着色，渲染器只需减去 `bgc=` 值并添加 `color=` 值。

如果 `color=` 未指定。 的 `bgc=` 属性被橱柜材料忽略；嵌入在 [!DNL vnc] 文件。
