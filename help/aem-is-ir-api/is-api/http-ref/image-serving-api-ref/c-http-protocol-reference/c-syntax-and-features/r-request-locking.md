---
description: 为了减少篡改请求的机会，提供了一种简单的锁定装置。
solution: Experience Manager
title: 请求锁定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 请求锁定{#request-locking}

为了减少篡改请求的机会，提供了一种简单的锁定装置。

如果设置了attribute：：RequestLock，则必须将锁定值附加到请求中，其形式为 `&xxxx`，其中xxxx是四位数的十六进制值。 此十六进制值是使用应用于 *修饰符* 部分（在“？”之后） 用于将URL路径与 *修饰符*)。 必须在请求完全经过http编码之后，但在（可选）进行模糊处理之前执行此操作。 在取消混淆请求后，服务器将对修饰符字符串使用相同的哈希算法（不包括最后5个字符，其中包含锁值）。 如果生成的密钥与锁定不匹配，则拒绝该请求。

>[!IMPORTANT]
>
>如果启用此功能，请注意，其使用存在某些限制，包括：<br>-Dynamic Media用户界面可能不会显示针对的正确详细信息 **[!UICONTROL 上次发布时间]** 字段。 但是，此影响不会影响发布。<br> — 目前，HLS视频流在以下情况下不起作用： **[!UICONTROL 请求模糊处理]** 和 **[!UICONTROL 请求锁定]** 已启用。<br> — 目前，某些Dynamic Media查看器在以下情况下不起作用： **[!UICONTROL 请求模糊处理]** 和 **[!UICONTROL 请求锁定]** 已启用。

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

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)， [请求模糊处理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)， [attribute：：RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
