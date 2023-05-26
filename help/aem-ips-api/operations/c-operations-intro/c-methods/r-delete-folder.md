---
description: 删除文件夹。
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 11%

---

# deleteFolder{#deletefolder}

删除文件夹。

语法

## 授权用户类型 {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对该文件夹及其所有子文件夹的读取和删除权限。

## 参数 {#section-a793c98a481a4f26ab50bc69b16b57e7}

**输入(deleteFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 文件夹所属公司的句柄。 |
| folderHandle | `xsd:string` | 是 | 要删除的文件夹的句柄。 |

**输出(deleteFolderParam)**

IPS API未返回此操作的响应。

## 示例 {#section-9d4617b322e8442d80e59be0f8714841}

此示例代码从公司的根目录中删除一个文件夹。 它需要一个文件夹句柄，您必须从另一个操作中获取该句柄。

**请求**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

无。
