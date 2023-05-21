---
description: server.xml中的Connector標籤支援密碼屬性，以限制可為SSL連線選擇的密碼。
solution: Experience Manager
title: 定義SSL加密
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
source-git-commit: 370444b85cb2636d109df4e2681e3e078d6f1e1a
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# 定義SSL加密{#defining-ssl-ciphers}

server.xml中的Connector標籤支援密碼屬性，以限制可為SSL連線選擇的密碼。

依預設，所有密碼都可使用。 此清單以逗號分隔，可包含以下任一值：

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

<!-- WEAK CQDOC-19433 `SSL_RSA_WITH_3DES_EDE_CBC_SHA` -->

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

<!-- WEAK CQDOC-19433 `TLS_RSA_WITH_AES_128_CBC_SHA` -->

如果有任何值錯誤，Tomcat會啟用每個單一密碼。 因此，在設定後務必使用外部工具檢查，以檢視實際啟用了哪些加密。

例如，下列設定僅會啟用「128位元」加密套件和以上版本：

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA"`
