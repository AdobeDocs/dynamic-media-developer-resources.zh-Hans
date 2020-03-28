---
description: 为了减少篡改请求的机会，提供了一种简单的锁定设备。
seo-description: 为了减少篡改请求的机会，提供了一种简单的锁定设备。
seo-title: 请求锁定
solution: Experience Manager
title: 请求锁定
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 请求锁定{#request-locking}

为了减少篡改请求的机会，提供了一种简单的锁定设备。

如果设置了属性：:RequestLock，则必须在请求中附加一个锁定值，其形式为 `&xxxx`xxxx是四位数的十六进制值。 此十六进制值是使用应用于请求修饰符部分的简单哈希 *算法* （在“?”之后）生成的。 它将URL路径与修饰符分 *开*)。 必须在请求完全http编码后，但在（可选）被模糊处理之前完成此操作。 在对请求进行去模糊处理后，服务器将对修饰符字符串使用相同的哈希算法（不包括最后5个字符，后者包含锁定值）。 如果生成的密钥与锁不匹配，则拒绝请求。

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

[HTTP编码](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7)，请 [求模糊化](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d)，属 [性：:RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
