---
title: 外部图像源
description: 图像服务支持访问外部HTTP和FTP服务器上的源图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90f96a76-e9f3-4ad0-84af-bc0d093acf19
TQID: 'https://experienceleague.adobe.com/doS6fbVfaXGtLVNBAmOkB-TquNmOc5B2B--IewouFDY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# 外部图像源{#foreign-image-sources}

图像服务支持访问外部HTTP和FTP服务器上的源图像。

要为`src=`或`mask=`命令指定外部URL，只需用大括号分隔整个嵌入式URL：

` …&src={ *[!DNL foreignUrl]*}&…`

允许使用完全绝对URL（如果已设置`attribute::AllowDirectUrls`）和相对`attribute::RootUrl`的URL。 如果嵌入了绝对URL并且属性： `AllowDirectUrls`为0，或者如果指定了相对URL并且`attribute::RootUrl`为空，则会发生错误。

服务器根据HTTP响应中包含的缓存标头来缓存外来图像。
