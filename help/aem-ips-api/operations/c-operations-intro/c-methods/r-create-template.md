---
description: 创建可以具有多个文本和图像图层的图层图像。
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 11%

---

# createTemplate{#createtemplate}

创建可以具有多个文本和图像图层的图层图像。

此 `urlModifier` 参数指定在URL上用户提供的任何命令之前应用的图像服务器目录中存储的图像服务器协议命令。 此 `urlPostApplyModifier` parameter指定在任何URL命令之后应用的协议命令，这会覆盖任何冲突的用户提供的设置。

## 授权用户类型 {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**输入(createTemplateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 模板所属的公司。 |
| folderHandle | `xsd:string` | 是 | 表示模板所在的文件夹的文件夹句柄。 |
| 名称 | `xsd:string` | 是 | 模板名称。 |
| 类型 | `xsd:string` | 是 | 模板类型。 |
| urlModifier | `xsd:string` | 是 | 指定存储在IS目录中的图像服务器命令，这些命令在URL上用户提供的任何命令之前应用。 |
| urlPostApplyModifier | `xsd:string` | 否 | 指定在任何URL命令之后应用的协议命令，这会覆盖任何冲突的用户提供的设置。 |

**输出(createTemplateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 模板的句柄。 |

## 示例 {#section-09adb4d2f0c944af875c4463a461f55d}

此代码示例在句柄指定的文件夹中创建名为 `APIcreateTemplate`， a `urlModifier`，和 `urlPostApplyModifier`. 响应会将句柄返回到新创建的模板。

**请求**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**响应**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
