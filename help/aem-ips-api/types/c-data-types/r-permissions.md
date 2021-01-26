---
description: 管理按组访问、修改、创建或删除资产的权限。
seo-description: 管理按组访问、修改、创建或删除资产的权限。
seo-title: 权限
solution: Experience Manager
title: 权限
topic: Dynamic Media Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 10%

---


# 权限{#permission}

管理按组访问、修改、创建或删除资产的权限。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | 组句柄。 |
| `*`groupName`*` | `xsd:string` | 群组名称. |
| `*`permissionType`*` | `xsd:string` | 权限类型的选项。 |
| `*`isAllowed`*` | `xsd:boolean` | 确定是否允许该权限。 |
| `*`isOverride`*` | `xsd:boolean` | 确定权限是否覆盖其他权限。 |

