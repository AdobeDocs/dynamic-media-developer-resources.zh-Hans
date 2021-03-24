---
description: 按组管理访问、修改、创建或删除资产的权限。
solution: Experience Manager
title: 权限
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---


# 权限{#permission}

按组管理访问、修改、创建或删除资产的权限。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 组句柄。 |
| `*`groupName`*` | `xsd:string` | 群组名称. |
| `*`permissionType`*` | `xsd:string` | 权限类型的选择。 |
| `*`isAllowed`*` | `xsd:boolean` | 确定是否允许该权限。 |
| `*`isOverride`*` | `xsd:boolean` | 确定权限是否覆盖其他权限。 |

