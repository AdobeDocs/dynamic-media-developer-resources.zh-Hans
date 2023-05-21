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
>新資料夾隸屬於Images資料夾，即使您指定 `/` 以指出公司的根目錄。

语法

## 授權的使用者型別 {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有上層資料夾的讀取/寫入許可權。

## 参数 {#section-c00d8d89cf114886a535056f2a1bf892}

**輸入(createFolder)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼 |
| 資料夾路徑 | `xsd:string` | 是 | 用來擷取葉層級資料夾和所有子資料夾的根資料夾。 如果排除，則使用公司根目錄。 |

**輸出(createFolderParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| folderHandle | `xsd:string` | 是 | 新資料夾的控制代碼。 |

## 示例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

此範常式式碼會在公司的根目錄下建立資料夾。 回應會傳回新建立資料夾的控制代碼。

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
