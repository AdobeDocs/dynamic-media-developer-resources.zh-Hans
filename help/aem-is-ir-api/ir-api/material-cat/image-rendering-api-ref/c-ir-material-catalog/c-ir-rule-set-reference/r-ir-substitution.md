---
title: 替换
description: 替换字符串元素。 <rule>元素中的可选。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
TQID: 'https://experienceleague.adobe.com/GqJBLso7oigoeCJ-0KQzFv2aeoAiVzumjlDTtjBSDI4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 3%

---

# 替换{#substitution}

替换字符串元素。 `<rule>`元素中的可选。

## 属性 {#section-d955eefc53eb4274861270669c01f9ca}

无。

## 数据 {#section-a2688866ed6d41279a8478886e511ae3}

替换字符串。

## 说明 {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

为路径或查询中匹配的字符串或子字符串定义替换字符串。

如果模式表达式包含子表达式（用括号分隔），则第一个匹配的子字符串将被替换为替换字符串。 如果模式表达式不包含子表达式，则将替换整个匹配的字符串。

如果`<expression>`为空或不存在，则替代字符串将附加到路径或查询中。

如果`<substitution>`为空，则将删除匹配的字符串或子字符串。 如果未指定`<substitution>`，则不会修改路径或查询字符串。

## 注意 {#section-90fe89bb17a04804b7ff3c93df082892}

替换字符串不得包含文字&lt;和&amp;字符。 这些保留字符可以分别使用`&`和`<`进行编码，或者整个字符串可以包含在XML `CDATA`部分中：

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`

