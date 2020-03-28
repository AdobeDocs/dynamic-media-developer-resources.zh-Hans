---
description: 创建一个预设视图，它确定用户可以看到的内容。 查看器可以是IPS中可用的任何类型。 预设视图在资产发布时应用。
seo-description: 创建一个预设视图，它确定用户可以看到的内容。 查看器可以是IPS中可用的任何类型。 预设视图在资产发布时应用。
seo-title: createViewerPreset
solution: Experience Manager
title: createViewerPreset
topic: Scene7 Image Production System API
uuid: 4160d2b0-6147-459f-830a-43c99b8dc196
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createViewerPreset{#createviewerpreset}

创建一个预设视图，它确定用户可以看到的内容。 查看器可以是IPS中可用的任何类型。 预设视图在资产发布时应用。

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 包含查看器预设和资产的公司的句柄。 |
| ` *`folderHandle`*` | `xsd:string` | 是 | 包含资产的文件夹的句柄。 |
| ` *`名称`*` | `xsd:string` | 是 | 查看器名称。 |
| ` *`类型`*` | `xsd:string` | 是 | 查看器类型. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | 否 | 一个数组，其中包含要应用预设的图像的名称、值和句柄。 |

**输出(createViewerPresetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`viewerPresetHandle`*` | `xsd:string` | 是 | 对查看器处理预设。 |

## 示例 {#section-c88ea63536f3461cbe4677ba53f875dd}

此代码示例创建视频播放器预设。 响应将返回预设的句柄。

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

