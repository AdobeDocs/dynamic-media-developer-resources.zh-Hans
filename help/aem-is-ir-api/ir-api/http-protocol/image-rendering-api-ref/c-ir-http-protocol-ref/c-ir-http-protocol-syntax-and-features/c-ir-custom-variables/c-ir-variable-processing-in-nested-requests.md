---
description: $var$引用可能出现在嵌套图像服务或图像渲染请求的花括号内的任何位置，包括“?”左侧 将路径与查询分开。
seo-description: $var$引用可能出现在嵌套图像服务或图像渲染请求的花括号内的任何位置，包括“?”左侧 将路径与查询分开。
seo-title: 嵌套请求中的变量处理
solution: Experience Manager
title: 嵌套请求中的变量处理
topic: Scene7 Image Serving - Image Rendering API
uuid: 2f3fefac-d45e-4c53-854f-1fe16d0cedd9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 嵌套请求中的变量处理{#variable-processing-in-nested-requests}

$var$引用可能出现在嵌套图像服务或图像渲染请求的花括号内的任何位置，包括“?”左侧 将路径与查询分开。

在进一步分析和处理嵌套请求之前，服务器会将这些引用替换为值( `catalog::Modifier` 来自URL或来自主图像目录)。

此外，URL中的所 `$ *[!DNL var]*=` 有定义都会转发到所 `catalog::Modifier` 有嵌套的图像服务和图像渲染请求。 这可确保所有变量定义都对所有模板可用，而不管嵌套级别如何。

无论嵌套级别如何，只能将单遍HTTP编码应用于要在嵌套图像渲染或图像服务请求中的任意位置替换的变量值。
