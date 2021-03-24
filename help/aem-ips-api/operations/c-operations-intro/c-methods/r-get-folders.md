---
description: 返回所有文件夹和子文件夹，从文件夹路径开始。 getFolders响应最多返回100,000个文件夹。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 8%

---


# getFolders{#getfolders}

返回所有文件夹和子文件夹，从文件夹路径开始。 getFolders响应最多返回100,000个文件夹。

## 文件夹{#section-66e344d5333f42f1b060a0cba25935c3}的用途

您可以使用文件夹组织子文件夹和资源。 所有文件夹和资产名称必须唯一。 共享相同名称的文件夹和资产会导致命名空间冲突，即使它们位于不同的文件夹层次结构中也是如此。
语法

## 授权用户类型{#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的手柄。 |
| `*`accessUserHandle`*` | `xsd:string` | 否 | 管理员用于模拟特定用户。 |
| `*`accessGroupHandle`*` | `xsd:string` | 否 | 按特定组过滤。 |
| `*`folderPath`*` | `xsd:string` | 否 | 要检索文件夹及所有子文件夹到叶级的根文件夹。 如果排除，则使用公司根。 |
| `*`assetTypeArray`*` | `types:StringArray` | 否 | 返回仅包含指定资产类型的文件夹。 |
| `*`responseFieldArray`*` | `types:StringArray` | 否 | 包含要包含在响应中的字段列表。 |
| `*`excludeFieldArray`*` | `types:StringArray` | 否 | 包含要从响应中排除的字段的列表。 |

**输出(getFoldersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | 否 | 与筛选条件匹配的文件夹数组。 响应限制为最多100,000个文件夹。 |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## 示例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

此代码示例返回一个数组，其中包含公司的所有文件夹以及每个文件夹的特定信息。

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

