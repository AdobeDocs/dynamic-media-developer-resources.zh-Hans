---
description: 為指定的資產設定影像伺服或影像演算通訊協定命令。 這些命令會修改資產的表示方式，而不會破壞資產。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

為指定的資產設定影像伺服或影像演算通訊協定命令。 這些命令會修改資產的表示方式，而不會破壞資產。

針對「影像伺服」，命令位在 `urlModifier` 引數會發佈在Modifier catalog欄位中，並在要求URL上指定的任何命令之前套用。 中的命令 `urlPostApplyModifier` 發佈至 `PostModifier` 目錄欄位並覆寫請求URL上或中的任何命令 `urlModifier`. 對於影像演算，命令位於 `urlModifier` 和 `urlPostApplyModifier` 串連並發佈至「修飾元目錄」欄位。

## 授權的使用者型別 {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**輸入(setUrlModifierParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控點。 |
| assetHandle | `xsd:string` | 是 | 資產控點。 |
| urlModifier | `xsd:string` | 否 | 在請求或之前，要套用的影像提供或影像演算通訊協定命令 `urlPostApplyModifier` 命令。 |
| urlPostApplyModifier | `xsd:string` | 否 | 之後要套用的影像提供或影像演算通訊協定命令 `urlModifier` 和request命令。 |

**輸出(setUrlModifierReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-801d4b9b986443f59a5783a3d6bf44aa}

**请求**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**响应**

无。
