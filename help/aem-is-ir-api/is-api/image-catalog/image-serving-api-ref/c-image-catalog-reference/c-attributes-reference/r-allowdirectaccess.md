---
description: 允許直接存取路徑型資產。
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

允許直接存取路徑型資產。

定義此屬性時，指定物件型別允許或限制以路徑為基礎的存取，取決於 `include` 或 `exclude` 關鍵字已使用。

>[!NOTE]
>
>如果 `AllowDirectAccess` 屬性未指定，預設值為 `exclude`.

* `include` 允許指定物件型別的存取權並限制其他所有物件型別的存取權。
* `exclude` 限制指定物件型別的存取權，並允許其他所有物件型別的存取權。

如果兩者都不 `include` 也不 `exclude` 已指定， `include` 為假設。

可以控制下列型別：

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## 示例 {#section-4c3765ebaa4245a799b454fc196f9237}

* 僅允許直接存取 `IS` 和 `STATIC` 物件型別

   `AllowDirectAccess=include:IS,STATIC`

* 允許直接存取所有物件型別，但 `IS` 和 `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* 允許直接存取 *否* 物件型別（即不包含任何物件）

   `AllowDirectAccess=include:`

* 允許直接存取 *全部* 物件型別（即不排除）

   `AllowDirectAccess=exclude:`

* 相當於 `include:IS,STATIC` (如果 `include`/ `exclude` 不存在， `include` 為假設)

   `AllowDirectAccess=IS,STATIC`

   請注意，是預設值，使用於 `AllowDirectAccess` 沒有為此公司指定屬性。

* 不包含任何專案，等同於 `include:` (如果 `include`/ `exclude` 不存在， `include` 為假設)

   `AllowDirectAccess=`
