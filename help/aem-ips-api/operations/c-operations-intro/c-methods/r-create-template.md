---
description: 创建可具有多个文本和图像图层的分层图像。
seo-description: 创建可具有多个文本和图像图层的分层图像。
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Dynamic Media Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 10%

---


# createTemplate{#createtemplate}

创建可具有多个文本和图像图层的分层图像。

`urlModifier`参数指定在URL上由用户提供的任何命令之前应用的图像服务器目录中存储的图像服务器协议命令。 `urlPostApplyModifier`参数指定在任何URL命令后应用的协议命令，这将覆盖任何与用户提供的设置冲突的设置。

## 授权用户类型{#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**输入(createTemplateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 模板所属的公司。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 表示模板所在文件夹的文件夹句柄。 |
| `*`name`*` | `xsd:string` | 是 | 模板名称。 |
| `*`类型`*` | `xsd:string` | 是 | 模板类型。 |
| `*`urlModifier`*` | `xsd:string` | 是 | 指定在IS目录中存储的图像服务器命令，这些命令在用户提供的URL命令之前应用。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 否 | 指定在任何URL命令后应用的协议命令，这将覆盖任何冲突的用户提供的设置。 |

**输出(createTemplateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 模板的句柄。 |

## 示例 {#section-09adb4d2f0c944af875c4463a461f55d}

此代码示例在句柄指定的文件夹中创建一个模板，名称为`APIcreateTemplate`、`urlModifier`和`urlPostApplyModifier`。 该响应会将句柄返回到新创建的模板。

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

