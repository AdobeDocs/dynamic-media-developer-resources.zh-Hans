---
description: 从文件夹路径开始返回所有文件夹和子文件夹。 getFolders响应返回的文件夹数最多为100,000个。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 8%

---

# getFolders{#getfolders}

从文件夹路径开始返回所有文件夹和子文件夹。 getFolders响应返回的文件夹数最多为100,000个。

## 文件夹的用途 {#section-66e344d5333f42f1b060a0cba25935c3}

利用文件夹，可组织子文件夹和资产。 所有文件夹和资产名称必须唯一。 共享相同名称的文件夹和资产将导致命名空间冲突，即使它们位于不同的文件夹层次结构中也是如此。
语法

## 授权用户类型 {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对文件夹的读取权限才能返回其上的数据。

## 参数 {#section-0c1976503eaa418a9226b51667901176}

**输入(getFoldersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`accessUserHandle`*` | `xsd:string` | 否 | 管理员用于模拟特定用户。 |
| `*`accessGroupHandle`*` | `xsd:string` | 否 | 按特定组过滤。 |
| `*`folderPath`*` | `xsd:string` | 否 | 用于将文件夹及所有子文件夹检索到叶级别的根文件夹。 如果排除，则使用公司根。 |
| `*`assetTypeArray`*` | `types:StringArray` | 否 | 返回仅包含指定资产类型的文件夹。 |
| `*`responseFieldArray`*` | `types:StringArray` | 否 | 包含要包含在响应中的字段列表。 |
| `*`excludeFieldArray`*` | `types:StringArray` | 否 | 包含要从响应中排除的字段列表。 |

**Output(getFoldersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | 否 | 与筛选条件匹配的文件夹数组。 响应最多限制为100,000个文件夹。 |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## 示例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

此代码示例会返回一个数组，其中包含公司的所有文件夹以及有关每个文件夹的特定信息。

**请求**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**响应**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```
