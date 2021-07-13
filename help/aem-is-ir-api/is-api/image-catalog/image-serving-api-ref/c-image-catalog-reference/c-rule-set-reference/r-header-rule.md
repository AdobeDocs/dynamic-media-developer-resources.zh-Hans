---
description: HTTP响应标头元素。 在<rule>元素中为可选项。
solution: Experience Manager
title: header
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 4%

---

# 标题{#header}

HTTP响应标头元素。 在`<rule>`元素中为可选。

## 属性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** :必需。指定HTTP标头的名称。

**`Action`= &quot;set&quot; |`"add"`**:可选。默认值为`"set"`，它会替换任何当前标头值。 指定`"add"`以附加以逗号分隔的标头值。

## 数据 {#section-a387f541396c49d99c29692a38032914}

标题值。

## 说明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允许添加新的HTTP响应标头，以及添加或替换预定义标头的值。 名称和值必须符合HTTP标准。 将不应用其他编码。

图像提供替换变量可用于标题名称和标题值中。 这允许从请求中控制两个字符串。

## 示例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

当在请求中将标头值指定为变量时，以下规则将应用自定义标头：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此规则由以下请求触发，请设置HTTP响应标头`Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
