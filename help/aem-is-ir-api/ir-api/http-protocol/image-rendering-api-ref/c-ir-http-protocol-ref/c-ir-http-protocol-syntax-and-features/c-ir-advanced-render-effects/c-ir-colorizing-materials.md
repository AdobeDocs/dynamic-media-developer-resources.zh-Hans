---
title: 色彩化材質
description: 大多數材質都可動態上色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 色彩化材質{#colorizing-materials}

大多數材質都可動態上色。

上色演演算法非常簡單，最適合色相範圍有限的材質影像。 若要將材質上色，轉譯器只會減去 `bgc=` 值並新增 `color=` 值至每個畫素值。

若有下列情況，則已停用色彩化： `color=` 未指定。 此 `bgc=` 屬性會被封包材料忽略；內嵌在封包材料中的基色值 [!DNL vnc] 會改用檔案。
