---
description: HTTP响应头元素。 在<rule>元素中为可选。
seo-description: HTTP响应头元素。 在<rule>元素中为可选。
seo-title: header
solution: Experience Manager
title: 标题
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---


# header{#header}

HTTP响应头元素。 在`<rule>`元素中为可选。

## 属性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** :必需。指定HTTP头的名称。

**`Action`= &quot;set&quot; |`"add"`**:可选。默认值为`"set"`，它替换任何当前标题值。 指定`"add"`以附加以逗号分隔的标题值。

## 数据 {#section-a387f541396c49d99c29692a38032914}

标题值。

## 说明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允许添加新的HTTP响应头以及添加或替换预定义头的值。 名称和值必须符合HTTP标准。 将不应用任何其他编码。

图像服务替换变量可用于标题名称和标题值。 这允许从请求控制两个字符串。

## 示例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

当请求中将标题值指定为变量时，以下规则将应用自定义标题：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此规则由以下请求触发，设置HTTP响应头`Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
