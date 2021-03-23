---
description: 将文件夹移到新位置。
seo-description: 将文件夹移到新位置。
seo-title: moveFolder
solution: Experience Manager
title: moveFolder
uuid: 424858c3-5796-4ae9-b5ad-fd50ddbee702
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 22%

---


# moveFolder{#movefolder}

将文件夹移到新位置。

语法

## 授权用户类型{#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-473c2e68bcc14a9ea2593bee26e679dd}

**输入(moveFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 文件夹句柄。 |
| `*`destFolderHandle`*` | `xsd:string` | 是 | 处理目标文件夹。 |

**输出(moveFolderReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 是 | 处理移动的文件夹。 |

## 示例 {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**请求**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**响应**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

