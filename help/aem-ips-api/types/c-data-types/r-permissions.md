---
description: 管理按组访问、修改、创建或删除资产的权限。
seo-description: 管理按组访问、修改、创建或删除资产的权限。
seo-title: 权限
solution: Experience Manager
title: 权限
topic: Scene7 Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Permission{#permission}

管理按组访问、修改、创建或删除资产的权限。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | 组句柄。 |
| ` *`groupName`*` | `xsd:string` | 群组名称. |
| ` *`permissionType`*` | `xsd:string` | 权限类型的选择。 |
| ` *`isAllowed`*` | `xsd:boolean` | 确定是否允许该权限。 |
| ` *`isOverride`*` | `xsd:boolean` | 确定权限是否覆盖其他权限。 |

