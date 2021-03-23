---
description: 查看器允许您将目录内容输出到打印机。
seo-description: 查看器允许您将目录内容输出到打印机。
seo-title: 打印功能
solution: Experience Manager
title: 打印功能
uuid: 4ff170a3-ce37-454f-b4b0-b323de3dc9c9
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---


# 打印功能{#print-feature}

查看器允许您将目录内容输出到打印机。

打印功能由工具栏中的专用按钮触发。 单击该按钮可让用户选择打印范围和每张纸的页数。

可以使用`printquality`配置参数调整打印质量。 请注意，不建议将`printquality`设置为显着高于默认值的值。 原因是它导致客户端系统上的Web浏览器占用的内存非常高。 另外，请确保为Dynamic Media Classic公司设置的最大图像响应大小大于配置的`printquality`值。

>[!NOTE]
>
>“打印”功能仅在桌面系统上可用，Internet Explorer 9除外。

