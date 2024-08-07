---
description: 为了减少篡改请求的机会，提供了一种简单的锁定装置。
solution: Experience Manager
title: 请求锁定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 请求锁定{#request-locking}

为了减少篡改请求的机会，提供了一种简单的锁定装置。

如果设置了attribute：：RequestLock，则必须以`&xxxx`的形式将锁定值附加到请求中，其中xxxx是四位十六进制值。 此十六进制值是使用应用于请求的&#x200B;*修饰符*&#x200B;部分（在“？”之后）的简单哈希算法生成的 用于将URL路径与&#x200B;*修饰符*&#x200B;分开。 必须在请求完全进行http编码之后，但在对其进行模糊处理（可选）之前执行此操作。 在取消混淆请求后，服务器对修饰符字符串使用相同的哈希算法（不包括最后5个字符，这些字符包含锁值）。 如果生成的键与锁定不匹配，则拒绝请求。

>[!IMPORTANT]
>
>如果启用此功能，请注意，其使用存在某些限制，包括：<br>- Dynamic Media用户界面可能无法显示&#x200B;**[!UICONTROL 上次发布]**&#x200B;字段的正确详细信息。 但是，此项影响不会影响发布。<br> — 当前，启用&#x200B;**[!UICONTROL 请求模糊处理]**&#x200B;和&#x200B;**[!UICONTROL 请求锁定]**&#x200B;时，HLS视频流不起作用。<br> — 当前，在启用&#x200B;**[!UICONTROL 请求模糊处理]**&#x200B;和&#x200B;**[!UICONTROL 请求锁定]**&#x200B;的情况下，某些Dynamic Media查看器无法工作。

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

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)，[请求模糊处理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)，[属性：：RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
