---
description: 查看器允许您将目录内容输出到打印机。
solution: Experience Manager
title: 打印功能
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 打印功能{#print-feature}

查看器允许您将目录内容输出到打印机。

打印功能由工具栏中的专用按钮触发。 单击按钮可让用户选择打印范围和每张页面的页数。

可以使用`printquality`配置参数调整打印质量。 请注意，不建议将`printquality`设置为显着高于默认值的值。 这是因为它导致客户端系统上的Web浏览器内存消耗非常高。 此外，请确保为您的Dynamic Media Classic公司设置的最大图像响应大小大于配置的`printquality`值。

>[!NOTE]
>
>打印功能仅在桌面系统上可用，但Internet Explorer 9除外。
