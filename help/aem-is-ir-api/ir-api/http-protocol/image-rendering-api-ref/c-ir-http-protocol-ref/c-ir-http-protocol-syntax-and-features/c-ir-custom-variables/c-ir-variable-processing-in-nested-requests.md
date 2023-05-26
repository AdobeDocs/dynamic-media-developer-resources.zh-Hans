---
title: 嵌套请求中的变量处理
description: $var$引用可能出现在嵌套图像服务或图像渲染请求的大括号内的任何位置，包括“？”左侧 将路径与查询分隔开。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 嵌套请求中的变量处理{#variable-processing-in-nested-requests}

$var$引用可能出现在嵌套图像服务或图像渲染请求的大括号内的任何位置，包括“？”左侧 将路径与查询分隔开。

服务器用值(来自URL或来自 `catalog::Modifier` )，然后进一步解析和处理嵌套请求。

此外，所有 `$ *[!DNL var]*=` url和中的定义 `catalog::Modifier` 转发到所有嵌套的图像服务和图像渲染请求。 这样做可确保所有变量定义都可用于所有模板，而不论嵌套级别如何。

无论嵌套级别如何，必须只对变量值应用单次HTTP编码，以便在嵌套图像渲染或图像服务请求中的任何位置替换这些变量值。
