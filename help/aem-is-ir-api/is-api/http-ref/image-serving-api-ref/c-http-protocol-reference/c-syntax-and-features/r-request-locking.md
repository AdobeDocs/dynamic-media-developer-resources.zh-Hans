---
description: 为了减少篡改请求的机会，提供了一种简单的锁定设备。
solution: Experience Manager
title: 请求锁定
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# 请求锁定{#request-locking}

为了减少篡改请求的机会，提供了一种简单的锁定设备。

如果设置了属性：:RequestLock，则必须在请求中附加一个锁定值（形式为`&xxxx`），其中xxxx是四位数的十六进制值。 此十六进制值是使用应用于请求&#x200B;*修饰符*&#x200B;部分（在“？”之后）的简单散列算法生成的 它将URL路径与&#x200B;*修饰符*&#x200B;分开。 必须在请求完全http编码后，但在（可选）将其模糊处理之前完成此操作。 在对请求进行去模糊处理后，服务器将对修饰符字符串使用相同的散列算法（不包括最后5个字符，后者包含锁定值）。 如果生成的密钥与锁定不匹配，则请求被拒绝。

>[!IMPORTANT]
>
>如果启用此功能，请注意，其使用存在某些限制，包括：<br>- Dynamic Media用户界面可能无法显示&#x200B;**[!UICONTROL 上次发布]**&#x200B;字段的正确详细信息。 但是，此影响不会影响发布。<br> — 当前，启用请求模糊处理和请&#x200B;**[!UICONTROL 求锁]** 定时， **[!UICONTROL HLS]** 视频流无效。<br> — 当前，启用“请求模糊处理”和“请 **[!UICONTROL 求锁]** 定”时， **[!UICONTROL 某些Dynamic Media]** 查看器无法工作。

C++示例代码生成请求锁定值：

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

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)，请 [求模糊](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)，属 [性：:RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
