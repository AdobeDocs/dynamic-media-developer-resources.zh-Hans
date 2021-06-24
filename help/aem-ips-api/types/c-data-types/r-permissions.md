---
description: 按组管理资产的访问、修改、创建或删除权限。
solution: Experience Manager
title: 权限
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 11%

---

# 权限{#permission}

按组管理资产的访问、修改、创建或删除权限。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 组句柄。 |
| `*`groupName`*` | `xsd:string` | 群组名称. |
| `*`permissionType`*` | `xsd:string` | 权限类型的选择。 |
| `*`允许`*` | `xsd:boolean` | 确定是否允许该权限。 |
| `*`isOverride`*` | `xsd:boolean` | 确定权限是否覆盖其他权限。 |
