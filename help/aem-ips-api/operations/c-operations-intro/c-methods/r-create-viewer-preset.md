---
description: 建立預設集檢視，決定使用者可以看到的內容。 檢視器可以是IPS中任何可用的型別。 資產發佈時會套用預設集檢視。
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 13%

---

# createViewerPreset{#createviewerpreset}

建立預設集檢視，決定使用者可以看到的內容。 檢視器可以是IPS中任何可用的型別。 資產發佈時會套用預設集檢視。

语法

## 授權的使用者型別 {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-aa6dc37e327541ebbfed7685cd8071ff}

**輸入(createViewerPresetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含檢視器預設集和資產的公司的控制代碼。 |
| folderHandle | `xsd:string` | 是 | 包含資產的資料夾的控制代碼。 |
| 名称 | `xsd:string` | 是 | 檢視器名稱。 |
| 类型 | `xsd:string` | 是 | 查看器类型. |
| configSettingArray | `types:ConfigSettingArray` | 否 | 一個陣列，內含您套用預設集的影像名稱、值和控點。 |

**輸出(createViewerPresetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | 是 | 檢視器預設集的操作框。 |

## 示例 {#section-c88ea63536f3461cbe4677ba53f875dd}

此程式碼範例會建立視訊播放器預設集。 回應會傳回預設集的控點。

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
