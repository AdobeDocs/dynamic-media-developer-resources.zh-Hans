---
description: 查看器允许您将目录内容输出到打印机。
solution: Experience Manager
title: 打印功能
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog搜索
role: Developer,Business Practitioner
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 打印功能{#print-feature}

查看器允许您将目录内容输出到打印机。

打印功能由工具栏中的专用按钮触发。 单击按钮可让用户选择打印范围和每张页数。

可使用`printquality`配置参数调整打印质量。 请注意，不建议将`printquality`设置为显着高于默认值的值。 原因是客户端系统上的Web浏览器会使内存消耗非常高。 此外，请确保为您的Dynamic Media Classic公司设置的最大图像响应大小大于配置的`printquality`值。

>[!NOTE]
>
>“打印”功能仅在桌面系统上可用，Internet Explorer 9除外。
