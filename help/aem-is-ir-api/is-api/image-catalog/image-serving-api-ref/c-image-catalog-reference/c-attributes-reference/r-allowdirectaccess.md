---
description: 允许直接访问基于路径的资源。
solution: Experience Manager
title: AllowDirectaccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# AllowDirectaccess{#allowdirectaccess}

允许直接访问基于路径的资源。

定义此属性后，根据是否使用`include`或`exclude`关键字，允许或限制指定对象类型的基于路径的访问。

>[!NOTE]
>
>如果未指定`AllowDirectAccess`特性，则默认值为`exclude`。

* `include`允许访问指定的对象类型并限制其他所有类型的访问。
* `exclude`限制指定对象类型的访问，并允许所有其他类型的访问。

如果未指定`include`或`exclude`，则假定为`include`。

可以控制以下类型：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 示例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 仅允许`IS`和`STATIC`对象类型的直接访问

  `AllowDirectAccess=include:IS,STATIC`

* 允许直接访问除`IS`和`STATIC``AllowDirectAccess=exclude:IS,STATIC`之外的所有对象类型

* 允许直接访问&#x200B;*no*&#x200B;对象类型（即，不包括）

  `AllowDirectAccess=include:`

* 允许直接访问&#x200B;*所有*&#x200B;对象类型（即不排除任何对象类型）

  `AllowDirectAccess=exclude:`

* 等同于`include:IS,STATIC`（如果不存在`include`/`exclude`，则假定为`include`）

  `AllowDirectAccess=IS,STATIC`

  请注意，如果未为此公司指定`AllowDirectAccess`特性，则使用此默认值。

* 不包含任何内容，等同于`include:`（如果`include`/`exclude`不存在，则假定为`include`）

  `AllowDirectAccess=`
