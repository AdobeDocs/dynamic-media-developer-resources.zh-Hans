---
description: 更新文件夹权限。
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 17%

---


# updateFolderPermissions{#updatefolderpermissions}

更新文件夹权限。

语法

## 授权用户类型{#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-339e6e17c5504e1ea79fbdc05f618050}

**输入(updateFolderPermissionsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 文件夹句柄。 |
| `*`updateChildren`*` | `xsd:boolean` | 是 | 确定是否使用为顶级文件夹设置的权限更新子级。 |
| `*`updateArray`*` | `types:PermissionUpdateArray` | 是 | 要应用到该文件夹的权限更新的数组。 |

**输出(updateFolderPermissionsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-c3fe4d4388674870a3856c35ef66b631}

**请求**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**响应**

无。
