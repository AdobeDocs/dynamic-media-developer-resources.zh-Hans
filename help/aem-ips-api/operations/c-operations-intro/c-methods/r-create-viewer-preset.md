---
description: 创建预设视图，以确定用户可以看到的内容。 查看器可以是IPS中可用的任何类型。 发布资产时，将应用预设视图。
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
TQID: 'https://experienceleague.adobe.com/0RlldrqgWyv0YeP-QqtiVqlDpWtGk60mOWf-w9ageYA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 12%

---

# createViewerPreset{#createviewerpreset}

创建预设视图，以确定用户可以看到的内容。 查看器可以是IPS中可用的任何类型。 发布资产时，将应用预设视图。

语法

## 授权用户类型 {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-aa6dc37e327541ebbfed7685cd8071ff}

**输入(createViewerPresetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含查看器预设和资产的公司的句柄。 |
| folderHandle | `xsd:string` | 是 | 包含资产的文件夹的句柄。 |
| 名称 | `xsd:string` | 是 | 查看器名称。 |
| 类型 | `xsd:string` | 是 | 查看器类型。 |
| configSettingArray | `types:ConfigSettingArray` | 否 | 一个数组，其中包含要应用预设的图像名称、值和句柄。 |

**输出(createViewerPresetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | 是 | 查看器预设的句柄。 |

## 示例 {#section-c88ea63536f3461cbe4677ba53f875dd}

此代码示例用于创建视频播放器预设。 响应将返回预设的句柄。

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**响应**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```
