---
description: HTTP响应头元素。 在<rule>元素中为可选。
solution: Experience Manager
title: header
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---


# header{#header}

HTTP响应头元素。 在`<rule>`元素中为可选。

## 属性 {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** :必填。指定HTTP头的名称。

**`Action`= &quot;set&quot; |`"add"`**:可选。默认值为`"set"`，它替换任何当前标头值。 指定`"add"`以附加以逗号分隔的标题值。

## 数据 {#section-a387f541396c49d99c29692a38032914}

标题值。

## 说明 {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

允许添加新的HTTP响应头以及添加或替换预定义标头的值。 名称和值必须符合HTTP标准。 将不应用任何其他编码。

图像服务替代变量可用于标题名称和标题值中。 这允许从请求控制两个字符串。

## 示例 {#section-cb5b738b9b93407cb2f4d35af3e59c02}

如果在请求中将标头值指定为变量，则以下规则将应用自定义标头：

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

此规则由以下请求触发，设置HTTP响应头`Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
