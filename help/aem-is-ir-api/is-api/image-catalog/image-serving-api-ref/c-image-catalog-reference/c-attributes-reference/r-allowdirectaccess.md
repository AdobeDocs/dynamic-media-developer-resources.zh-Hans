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

定义此属性后，将允许或限制指定对象类型基于路径的访问，具体取决于 `include` 或 `exclude` 使用关键字。

>[!NOTE]
>
>如果 `AllowDirectAccess` 未指定属性，默认值为 `exclude`.

* `include` 允许访问指定的对象类型并限制其他所有对象的访问。
* `exclude` 限制指定对象类型的访问，并允许所有其他类型的访问。

如果两者均不 `include` 也不 `exclude` 已指定， `include` 是假定的。

可以控制以下类型：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 示例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 仅允许直接访问 `IS` 和 `STATIC` 对象类型

  `AllowDirectAccess=include:IS,STATIC`

* 允许直接访问所有对象类型，但 `IS` 和 `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* 允许直接访问 *否* 对象类型（即不包括）

  `AllowDirectAccess=include:`

* 允许直接访问 *所有* 对象类型（即不排除任何对象）

  `AllowDirectAccess=exclude:`

* 相当于 `include:IS,STATIC` (如果 `include`/ `exclude` 不存在， `include` 假设为)

  `AllowDirectAccess=IS,STATIC`

  请注意，是默认值，如果 `AllowDirectAccess` 没有为此公司指定属性。

* 不包含任何内容，等同于 `include:` (如果 `include`/ `exclude` 不存在， `include` 假设为)

  `AllowDirectAccess=`
