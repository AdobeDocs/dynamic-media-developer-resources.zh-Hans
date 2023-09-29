---
title: header
description: HTTP响应标头元素。 中的可选 <rule> 元素。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# header{#header}

HTTP响应标头元素。 中的可选 `<rule>` 元素。

## 属性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*文本*&quot;** ：必填。 指定HTTP标头的名称。

**`Action`= &quot;set&quot; |`"add"`**：可选。 默认为 `"set"`，以替换任何当前标题值。 指定 `"add"` 以便附加标头值，并用逗号分隔。

## 数据 {#section-a387f541396c49d99c29692a38032914}

标头值。

## 说明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允许添加新的HTTP响应标头以及添加或替换预定义标头的值。 名称和值必须符合HTTP标准。 不应用其他编码。

可以在标头名称和标头值中使用图像服务替代变量。 这允许从请求中控制两个字符串。

## 示例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

在请求中将标头值指定为变量时，以下规则会应用自定义标头：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此规则由以下请求触发，其中设置HTTP响应标头 `Edge-Control::no-store`：

`http://server/is/image/cat/id?$Edge-Control=no-store`
