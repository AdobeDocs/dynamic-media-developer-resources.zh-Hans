---
description: 创建文件夹。
seo-description: 创建文件夹。
seo-title: 建立資料夾
solution: Experience Manager
title: 建立資料夾
topic: Dynamic Media Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 22%

---


# [!DNL createFolder]{#createfolder}

创建文件夹。

>[!NOTE]
>
>新文件夹与“图像”文件夹下属，即使您指定`/`来指示公司的根。

语法

## 授权用户类型{#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对父文件夹的读／写权限。

## 参数 {#section-c00d8d89cf114886a535056f2a1bf892}

**输入(createFolder)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司 |
| `*`folderPath`*` | `xsd:string` | 是 | 用于检索文件夹和所有子文件夹到叶级别的根文件夹。 如果排除，则使用公司根。 |

**输出(createFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | 是 | 处理新文件夹。 |

## 示例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

此示例代码在公司的根中创建文件夹。 响应将返回新创建的文件夹的句柄。

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

