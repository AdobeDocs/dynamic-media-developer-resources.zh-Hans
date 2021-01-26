---
description: 重命名文件夹。
seo-description: 重命名文件夹。
seo-title: renameFolder
solution: Experience Manager
title: renameFolder
topic: Dynamic Media Image Production System API
uuid: 7d190a57-1d81-4f41-9205-b8ffdf7330ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 21%

---


# renameFolder{#renamefolder}

重命名文件夹。

语法

## 授权用户类型{#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写权限。

## 参数 {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**输入(renameFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理要重命名的文件夹的公司。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 处理文件夹。 |
| `*`folderName`*` | `xsd:string` | 是 | 新文件夹名称。 |

**输出(renameFolderReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 是 | 处理重命名的文件夹。 |

## 示例 {#section-98bdd2f88d164f488676e90aba1dc864}

此代码示例重命名文件夹。

**请求**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**响应**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```

