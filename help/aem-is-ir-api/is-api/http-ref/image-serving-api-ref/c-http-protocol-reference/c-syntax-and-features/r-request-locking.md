---
description: 为了减少篡改请求的机会，提供了一种简单的锁定装置。
solution: Experience Manager
title: 请求锁定
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 请求锁定{#request-locking}

为了减少篡改请求的机会，提供了一种简单的锁定装置。

如果设置了attribute:RequestLock ，则必须将锁值以`&xxxx`的形式附加到请求中，其中xxxx是四位数的十六进制值。 此十六进制值是使用一个简单的哈希算法生成的，该算法应用于请求的&#x200B;*修饰符*&#x200B;部分（在“？”之后） 将URL路径与&#x200B;*修饰符*&#x200B;分隔开。 必须在请求经过完全http编码后，但在（可选）进行模糊处理之前，完成此操作。 在对请求进行去模糊处理后，服务器将对修饰符字符串（不包括最后5个字符，其中包含锁定值）使用相同的哈希算法。 如果生成的密钥与锁定不匹配，则请求将被拒绝。

>[!IMPORTANT]
>
>如果启用此功能，请注意，其使用存在某些限制，包括以下内容：<br> - Dynamic Media用户界面可能无法显示&#x200B;**[!UICONTROL 上次发布]**&#x200B;字段的正确详细信息。 但是，此影响不会影响发布。<br> — 目前，在启用请求模糊处理和请求锁定&#x200B;**[!UICONTROL 后，]** HLS视 **[!UICONTROL 频流]** 无法正常工作。<br> — 目前，在启用请求模糊处理和请求锁 **[!UICONTROL 定]** 后，某些Dynamic Media **[!UICONTROL 查看器]** 不起作用。

用于生成请求锁定值的C++示例代码：

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## 另请参阅 {#section-a6d45406c0354669ac581793e4fa8436}

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)、 [请求模糊处理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)、 [属性：:RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
