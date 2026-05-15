---
description: 查看器允许您将目录内容输出到打印机。
solution: Experience Manager
title: 打印功能
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
TQID: 'https://experienceleague.adobe.com/mbsxiwsrZch87oSFFhXUNp892iQSmfyAFaY7bzDn2MM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 0%

---

# 打印功能{#print-feature}

查看器允许您将目录内容输出到打印机。

打印功能由工具栏中的专用按钮触发。 单击按钮可让用户选择打印范围和每张页面的页数。

可以使用`printquality`配置参数调整打印质量。 请注意，不建议将`printquality`设置为显着高于默认值的值。 这是因为它导致客户端系统上的Web浏览器内存消耗非常高。 此外，请确保为您的Dynamic Media Classic公司设置的最大图像响应大小大于配置的`printquality`值。

>[!NOTE]
>
>打印功能仅在桌面系统上可用，但Internet Explorer 9除外。
