---
title: 打印功能
description: 查看器允许您将目录内容输出到打印机。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# 打印功能{#print-feature}

查看器允许您将目录内容输出到打印机。

打印功能由工具栏中的专用按钮触发。 单击按钮可让用户选择打印范围和每张页面的页数。

打印质量可通过以下方式调整 `printquality` 配置参数。 设置 `printquality` 不建议使用高于默认值的值。 原因在于，它导致客户端系统上的Web浏览器内存消耗过高。 此外，请确保为您的Dynamic Media Classic公司设置的最大图像响应大小大于配置的 `printquality` 值。

>[!NOTE]
>
>打印功能仅在桌面系统上可用，但Internet Explorer 9除外。
