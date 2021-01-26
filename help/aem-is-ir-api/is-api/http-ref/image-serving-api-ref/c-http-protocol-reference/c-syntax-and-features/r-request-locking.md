---
description: 为了减少篡改请求的机会，提供了一种简单的锁定装置。
seo-description: 为了减少篡改请求的机会，提供了一种简单的锁定装置。
seo-title: 请求锁定
solution: Experience Manager
title: 请求锁定
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# 请求锁定{#request-locking}

为了减少篡改请求的机会，提供了一种简单的锁定装置。

如果属性：:RequestLock已设置，则必须在请求中附加一个锁定值（形式为`&xxxx`）,xxxx为四位数的十六进制值。 此十六进制值是使用应用于请求&#x200B;*修饰符*&#x200B;部分（在“?”之后）的简单哈希算法生成的 它将URL路径与&#x200B;*修饰符*&#x200B;分开。 必须在请求完全http编码后（可选）模糊处理前执行此操作。 在对请求进行去模糊处理后，服务器将对修饰符字符串使用相同的哈希算法（不包括最后5个字符，后者包含锁定值）。 如果生成的密钥与锁不匹配，则拒绝请求。

>[!IMPORTANT]
>
>如果启用此功能，请注意其使用存在以下某些限制：<br>-Dynamic Media用户界面可能无法显示&#x200B;**[!UICONTROL 上次发布时间]**&#x200B;字段的正确详细信息。 但是，此影响不会影响发布。<br>-当前，启用请求模糊处理和请&#x200B;**[!UICONTROL 求锁]** 定时， **[!UICONTROL HLS视]** 频流无法工作。<br>-目前，启用请求模糊处理和请求锁定 **[!UICONTROL 后，某]** 些Dynamic Media查 **[!UICONTROL 看]** 器将无法工作。

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

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [请求模糊](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)，属 [性：:RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
