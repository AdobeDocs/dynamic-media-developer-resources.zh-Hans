---
title: 嵌套请求中的变量处理
description: $var$引用可能出现在嵌套图像服务或图像渲染请求的大括号内的任何位置，包括在“？”左侧，该左侧将路径与查询分开。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# 嵌套请求中的变量处理{#variable-processing-in-nested-requests}

$var$引用可能出现在嵌套图像服务或图像渲染请求的大括号内的任何位置，包括在“？”左侧，该左侧将路径与查询分开。

在进一步解析和处理嵌套请求之前，服务器会将这些引用替换为来自URL或主图像目录的`catalog::Modifier`的值。

此外，URL和`catalog::Modifier`中的所有`$ *[!DNL var]*=`定义都将转发到所有嵌套的图像服务和图像渲染请求。 这样做可确保所有变量定义都可用于所有模板，而不管嵌套级别如何。

无论嵌套级别如何，必须只对变量值应用单次HTTP编码，该值将在嵌套图像渲染或图像服务请求中的任意位置被替换。
