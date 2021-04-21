---
description: 目录数据文件可以具有任何名称和文件后缀（.ini除外）。
solution: Experience Manager
title: 目录数据文件
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# 目录数据文件{#catalog-data-files}

目录数据文件可以具有任何名称和文件后缀（.ini除外）。

可使用支持制表符分隔的文本数据文件（如Microsoft Excel和Access）的应用程序轻松维护目录数据文件。

目录数据文件本质上是二维表，由标头记录组成，标识数据列和任意数量的数据记录（行）。 标题和数据记录中的字段均以单个`<TAB>`字符分隔。 记录由单个`<CR>`（ASCII代码0xD）、单个`<LF>`（ASCII代码0xA）或`<CR><LF>`对分隔。

标题记录必须包含每个数据字段的确切名称。 标题行中不允许使用空字段。 数据字段名称不区分大小写。 所有字段名称必须唯一。

标题和数据记录中不允许除`<TAB>`字段分隔符之外的空格。

在数据记录中，两个相邻的`<TAB>`字符表示一个空字段。 空字段将从目录属性或服务器默认值继承默认值。

除非数据值为文本类型且用单引号或多次引号括起来，否则数据字段不得包含`<CR>`、`<LF>`或`<TAB>`字符。 数据字段不得进行HTTP编码。

除非另有说明，否则同一字段中的多个数据值用逗号(“，”)分隔。

名称开始为“。”的列 被忽略；这允许将数据存储在“图像渲染”不感兴趣的材料目录中。 标题名称未知的列将被忽略，并在日志文件中写入警告。

字段名称可能由ASCII字母、数字以及“ — ”和“_”的任意组合组成。

一个或多个列可用作索引键。 如果同一密钥在同一数据文件中多次发生，则以后的实例为准。
