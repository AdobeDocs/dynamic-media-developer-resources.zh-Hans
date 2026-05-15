---
description: 本节列出了为特定目的而保留的字符。
solution: Experience Manager
title: 保留的字符
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 76483f3f-f98b-471d-9c5d-49fa22eaf8a3
TQID: 'https://experienceleague.adobe.com/6TZRC5--KMRFGR550J9XIthoQruVkwE1UyiISlpMxTg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# 保留的字符{#reserved-characters}

本节列出了为特定目的而保留的字符。

RTF使用大括号“`{`”和“`}`”作为组分隔符。 它们必须成对出现，并且可以嵌套。 要在文本字符串中显示大括号，请分别使用“`\{`”和“`\}`”。

>[!NOTE]
>
>您必须对RTF中使用的所有大括号进行URL编码。

反斜杠“\”用于引入RTF命令和关键字。 要显示反斜线，请使用`'\\'`。
