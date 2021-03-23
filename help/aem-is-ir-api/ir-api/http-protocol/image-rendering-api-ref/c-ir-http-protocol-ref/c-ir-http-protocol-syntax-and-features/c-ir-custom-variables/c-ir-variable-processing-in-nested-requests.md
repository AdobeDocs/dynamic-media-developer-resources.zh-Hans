---
description: $var$引用可能发生在嵌套图像服务或图像渲染请求的花括号内的任何位置，包括“？”左侧 将路径与查询分离。
seo-description: $var$引用可能发生在嵌套图像服务或图像渲染请求的花括号内的任何位置，包括“？”左侧 将路径与查询分离。
seo-title: 嵌套请求中的变量处理
solution: Experience Manager
title: 嵌套请求中的变量处理
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# 嵌套请求中的变量处理{#variable-processing-in-nested-requests}

$var$引用可能发生在嵌套图像服务或图像渲染请求的花括号内的任何位置，包括“？”左侧 将路径与查询分离。

在进一步分析和处理嵌套请求之前，服务器将这些引用替换为值（来自URL或主图像目录的`catalog::Modifier`）。

此外，来自url和`catalog::Modifier`的所有`$ *[!DNL var]*=`定义都将转发到所有嵌套的图像服务和图像渲染请求。 这可确保所有模板都可以使用所有变量定义，而不管嵌套级别如何。

无论嵌套级别如何，只能对要在嵌套图像渲染或图像服务请求中的任意位置替换的变量值应用单遍HTTP编码。
