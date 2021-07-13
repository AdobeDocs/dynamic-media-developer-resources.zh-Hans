---
description: $var$引用可能出现在嵌套图像提供或图像渲染请求的大括号内的任何位置，包括“？”的左侧 将路径与查询分开。
solution: Experience Manager
title: 嵌套请求中的变量处理
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# 嵌套请求中的变量处理{#variable-processing-in-nested-requests}

$var$引用可能出现在嵌套图像提供或图像渲染请求的大括号内的任何位置，包括“？”的左侧 将路径与查询分开。

在进一步解析和处理嵌套请求之前，服务器会将这些引用替换为值（来自主图像目录的url或`catalog::Modifier`）。

此外， URL中的所有`$ *[!DNL var]*=`定义和`catalog::Modifier`定义都会转发到所有嵌套的图像提供和图像呈现请求。 这可确保所有变量定义都可用于所有模板，而不考虑嵌套级别。

无论嵌套级别如何，都只能对变量值应用单遍HTTP编码，这些变量值将在嵌套图像渲染或图像服务请求中的任意位置替换。
