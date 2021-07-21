---
description: 将文件夹移到新位置。
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic，SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 26%

---

# moveFolder{#movefolder}

将文件夹移到新位置。

语法

## 授权用户类型 {#section-7f1979fb5e504bdea3a8df01101b50c3}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 对公司负责。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 文件夹句柄。 |
| `*`destFolderHandle`*` | `xsd:string` | 是 | 处理到目标文件夹。 |

**输出(moveFolderReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 是 | 处理已移动的文件夹。 |

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
