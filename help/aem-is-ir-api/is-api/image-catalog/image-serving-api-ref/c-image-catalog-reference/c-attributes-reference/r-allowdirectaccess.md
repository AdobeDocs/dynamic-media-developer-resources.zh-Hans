---
description: 允许直接访问基于路径的资产。
seo-description: 允许直接访问基于路径的资产。
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AllowDirectAccess{#allowdirectaccess}

允许直接访问基于路径的资产。

定义此属性时，将允许或限制对指定对象类型的基于路径的访问，具体取决于是使 `include` 用 `exclude` 或关键字。

>[!NOTE]
>
>如果未 `AllowDirectAccess` 指定属性，则默认值为 `exclude`。

* `include` 允许访问指定的对象类型，并限制所有其他对象的访问。
* `exclude` 限制对指定对象类型的访问，并允许对所有其他对象类型的访问。

如果既未 `include` 指 `exclude` 定也未指 `include` 定，则假定。

可以控制以下类型：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 示例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 仅允许对象类型和对 `IS` 象类 `STATIC` 型直接访问

   `AllowDirectAccess=include:IS,STATIC`

* 允许直接访问除和之外的所有对象类 `IS` 型 `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* 不允许直接访 *问任何* 对象类型（即不包括任何对象）

   `AllowDirectAccess=include:`

* 允许直接访 *问所有* 对象类型（即不排除无）

   `AllowDirectAccess=exclude:`

* 等效 `include:IS,STATIC` 于(如 `include`果/ `exclude` 不存在，则假 `include` 定)

   `AllowDirectAccess=IS,STATIC`

   请注意，如果未指定此公司的属性， `AllowDirectAccess` 则使用的默认值。

* 包括none，等 `include:` 同于(如果 `include`/ `exclude` 不存在，则假 `include` 定)

   `AllowDirectAccess=`

