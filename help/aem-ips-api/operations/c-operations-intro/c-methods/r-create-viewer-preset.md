---
description: 创建一个预设视图，以确定用户可以查看的内容。 IPS中可提供任何类型的查看器。 资产发布后，将应用预设视图。
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic，SDK/API，查看器预设
role: Developer,Administrator
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 13%

---

# createViewerPreset{#createviewerpreset}

创建一个预设视图，以确定用户可以查看的内容。 IPS中可提供任何类型的查看器。 资产发布后，将应用预设视图。

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
| `*`companyHandle`*` | `xsd:string` | 是 | 包含查看器预设和资产的公司句柄。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 包含资产的文件夹的句柄。 |
| `*`name`*` | `xsd:string` | 是 | 查看器名称。 |
| `*`类型`*` | `xsd:string` | 是 | 查看器类型. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 否 | 一个数组，其中包含要应用预设的图像的名称、值和句柄。 |

**Output(createViewerPresetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | 是 | 将预设处理到查看器。 |

## 示例 {#section-c88ea63536f3461cbe4677ba53f875dd}

此代码示例将创建一个视频播放器预设。 响应将返回预设的句柄。

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
