---
description: 返回分层树结构中的文件夹和子文件夹。 getFolderTree响应最多限制为100,000个文件夹
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 9%

---


# getFolderTree{#getfoldertree}

返回分层树结构中的文件夹和子文件夹。 getFolderTree响应最多限制为100,000个文件夹

语法

## 授权用户类型{#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对文件夹的读取权限才能返回其上的数据。

## 参数 {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**输入(getFolderTreeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的手柄。 |
| `*`accessUserHandle`*` | `xsd:string` | 否 | 仅由管理员用来模拟特定用户。 |
| `*`accessGroupHandle`*` | `xsd:string` | 否 | 用于按特定组(包括公司所属的任何组)进行筛选。 |
| `*`folderPath`*` | `xsd:string` | 否 | 要检索文件夹及所有子文件夹到叶级的根文件夹。 如果排除，则使用公司根。 |
| `*`深度`*` | `xsd:int` | 是 | 值为零将获取顶级文件夹。 任何其他值都指定要降入树的深度。 |
| `*`assetTypeArray`*` | `types:StringArray` | 否 | 返回仅包含指定资产类型的文件夹。 |
| `*`responseFieldArray`*` | `types:StringArray` | 否 | 包含要包含在响应中的字段列表。 |
| `*`excludeFieldArray`*` | `types:StringArray` | 否 | 包含要在响应中排除的字段列表。 |

**输出(getFolderTreeReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`文件夹`*` | `types:folders` | 否 | 树结构中文件夹的层次结构。 响应限制为最多100,000个文件夹。 |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## 示例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

此代码示例使用公司句柄和深度参数来确定响应应返回的深度级别。 响应包含文件夹和子文件夹数组。 将深度值设置为较小的数字，以在文件夹树中进行更深入的搜索。

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

