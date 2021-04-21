---
description: 查看器允许您将目录内容输出到打印机。
solution: Experience Manager
title: 打印功能
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# 打印功能{#print-feature}

查看器允许您将目录内容输出到打印机。

打印功能由工具栏中的专用按钮触发。 单击该按钮可让用户选择打印范围和每张纸的页数。

可以使用`printquality`配置参数调整打印质量。 请注意，不建议将`printquality`设置为显着高于默认值的值。 原因是它导致客户端系统上的Web浏览器占用的内存非常高。 另外，请确保为Dynamic Media Classic公司设置的最大图像响应大小大于配置的`printquality`值。

>[!NOTE]
>
>“打印”功能仅在桌面系统上可用，Internet Explorer 9除外。

