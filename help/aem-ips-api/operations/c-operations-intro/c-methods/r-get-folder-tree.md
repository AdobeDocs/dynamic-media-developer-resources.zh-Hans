---
description: 以分层树结构返回文件夹和子文件夹。 getFolderTree响应限制为最多100,000个文件夹
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# getFolderTree{#getfoldertree}

以分层树结构返回文件夹和子文件夹。 getFolderTree响应限制为最多100,000个文件夹

语法

## 授权用户类型 {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有文件夹的读取权限才能返回文件夹上的数据。

## 参数 {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**输入(getFolderTreeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的把手。 |
| accessUserHandle | `xsd:string` | 否 | 仅供管理员用于模拟特定用户。 |
| accessGroupHandle | `xsd:string` | 否 | 用于按特定组进行筛选，包括公司所属的任何组。 |
| 文件夹路径 | `xsd:string` | 否 | 用于检索叶级别的文件夹和所有子文件夹的根文件夹。 如果排除，则使用公司根目录。 |
| 深度 | `xsd:int` | 是 | 如果值为0，则获取顶级文件夹。 任何其他值均指定下降到树中的深度。 |
| assetTypeArray | `types:StringArray` | 否 | 返回仅包含指定资源类型的文件夹。 |
| responseFieldArray | `types:StringArray` | 否 | 包含要包含在响应中的字段列表。 |
| excludeFieldArray | `types:StringArray` | 否 | 包含要在响应中排除的字段列表。 |

**输出(getFolderTreeReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 文件夹 | `types:folders` | 否 | 树结构中的文件夹层次结构。 响应最多可包含100,000个文件夹。 |
| permissionSetArray | `types:PermissionSetArray` |  |  |

## 示例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

此代码示例使用公司句柄和深度参数来确定响应应返回的深度级别。 响应包含具有相关内容的文件夹和子文件夹数组。 将深度值设置为较小的数字，以便在文件夹树中更深入地搜索。

**请求**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**响应**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```
