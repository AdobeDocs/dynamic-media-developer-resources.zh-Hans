---
title: 建立資料夾
description: 创建文件夹。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 19%

---

# [!DNL createFolder]{#createfolder}

创建文件夹。

>[!NOTE]
>
>新文件夹对于Images文件夹下属，即使您指定 `/` 以指示公司的根。

语法

## 授权用户类型 {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对父文件夹的读/写访问权限。

## 参数 {#section-c00d8d89cf114886a535056f2a1bf892}

**输入(createFolder)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 对公司的处理 |
| folderPath | `xsd:string` | 是 | 用于将文件夹及所有子文件夹检索到叶级别的根文件夹。 如果排除，则使用公司根。 |

**输出(createFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| folderHandle | `xsd:string` | 是 | 新文件夹的处理。 |

## 示例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

此示例代码在公司根目录下创建一个文件夹。 响应会返回新创建文件夹的句柄。

**请求**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**响应**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
