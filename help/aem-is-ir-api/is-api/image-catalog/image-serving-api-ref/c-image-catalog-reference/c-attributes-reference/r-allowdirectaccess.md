---
description: 允许直接访问基于路径的资产。
seo-description: 允许直接访问基于路径的资产。
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

允许直接访问基于路径的资产。

定义此属性后，将允许或限制指定对象类型的基于路径的访问，具体取决于是使用`include`还是`exclude`关键字。

>[!NOTE]
>
>如果未指定`AllowDirectAccess`属性，则默认值为`exclude`。

* `include` 允许访问指定的对象类型，并限制所有其他对象的访问。
* `exclude` 限制对指定对象类型的访问，并允许对所有其他对象类型进行访问。

如果既未指定`include`也未指定`exclude`，则假定`include`。

可以控制以下类型：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 示例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 仅允许对`IS`和`STATIC`对象类型进行直接访问

   `AllowDirectAccess=include:IS,STATIC`

* 允许直接访问除`IS`和`STATIC``AllowDirectAccess=exclude:IS,STATIC`之外的所有对象类型

* 允许对&#x200B;*no*&#x200B;对象类型进行直接访问（即无）

   `AllowDirectAccess=include:`

* 允许直接访问&#x200B;*所有*&#x200B;对象类型（即不排除）

   `AllowDirectAccess=exclude:`

* 等效于`include:IS,STATIC`（如果`include`/ `exclude`不存在，则假定`include`）

   `AllowDirectAccess=IS,STATIC`

   请注意，这是默认值，如果未为此公司指定`AllowDirectAccess`属性，则使用它。

* 无，等效于`include:`（如果`include`/ `exclude`不存在，则假定`include`）

   `AllowDirectAccess=`

