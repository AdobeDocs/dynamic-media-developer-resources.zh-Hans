---
description: 删除文件夹。
seo-description: 删除文件夹。
seo-title: deleteFolder
solution: Experience Manager
title: deleteFolder
uuid: 76af65fb-86ef-43e2-bfec-3682acf0afe6
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 10%

---


# deleteFolder{#deletefolder}

删除文件夹。

语法

## 授权用户类型{#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对文件夹及其所有子文件夹的读取和删除访问权限。

## 参数 {#section-a793c98a481a4f26ab50bc69b16b57e7}

**输入(deleteFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 文件夹所属公司的句柄。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 要删除的文件夹的句柄。 |

**输出(deleteFolderParam)**

IPS API不返回此操作的响应。

## 示例 {#section-9d4617b322e8442d80e59be0f8714841}

此示例代码从公司的根中删除文件夹。 它需要一个文件夹句柄，您必须从其他操作获取该句柄。

**请求**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

无。
