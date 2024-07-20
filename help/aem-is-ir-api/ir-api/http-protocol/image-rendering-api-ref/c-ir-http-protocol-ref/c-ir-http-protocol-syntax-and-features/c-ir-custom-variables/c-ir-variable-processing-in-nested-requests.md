---
title: 嵌套请求中的变量处理
description: $var$引用可能出现在嵌套图像服务或图像渲染请求的大括号内的任何位置，包括“？”的左侧 将路径与查询分开。
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

$var$引用可能出现在嵌套图像服务或图像渲染请求的大括号内的任何位置，包括“？”的左侧 将路径与查询分开。

在进一步解析和处理嵌套请求之前，服务器会将这些引用替换为来自URL或主图像目录的`catalog::Modifier`的值。

此外，URL和`catalog::Modifier`中的所有`$ *[!DNL var]*=`定义都将转发到所有嵌套的图像服务和图像渲染请求。 这样做可确保所有变量定义都可用于所有模板，而不管嵌套级别如何。

无论嵌套级别如何，必须只对变量值应用单次HTTP编码，该值将在嵌套图像渲染或图像服务请求中的任意位置被替换。
