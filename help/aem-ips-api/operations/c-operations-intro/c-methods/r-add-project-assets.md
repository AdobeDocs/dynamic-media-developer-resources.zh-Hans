---
description: 向项目添加一个或多个资源。
seo-description: 向项目添加一个或多个资源。
seo-title: addProjectAssets
solution: Experience Manager
title: addProjectAssets
topic: Scene7 Image Production System API
uuid: 48abea17-058e-4469-bb16-0abee8ef5214
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 11%

---


# addProjectAssets{#addprojectassets}

向项目添加一个或多个资源。

语法

## 授权用户类型{#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-20d498e971b6466298e60c8a77fc32b2}

**输入(addProjectAssetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 处理与当前项目关联的公司。 |
| ` *`projectHandle`*` | `xsd:string` | 是 | 处理要向其添加资产的项目。 |
| ` *`projectHandleArray`*` | `xsd:HandleArray` | 是 | 您要添加到当前项目的资源数组。 |

**输出(addProjectAssetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 是 | 已成功添加的资产数。 |
| ` *`warningCount`*` | `xsd:int` | 是 | 操作尝试向项目添加资产时生成的警告数。 |
| ` *`errorCount`*` | `xsd:int` | 是 | 操作尝试向项目添加资产时生成的错误数。 |
| ` *`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | 否 | 资产在操作尝试将资产添加到项目时生成的警告数组。 |
| ` *`companyHandle`*` | `xsd:AssetOperationFaultArray` | 否 | 资产在操作尝试将资产添加到项目时生成的错误数组。 |

## 示例 {#section-bee5be2402f54cb9a3a02cc07def4135}

此示例将资产句柄数组中的单个资产（由其句柄引用）添加到请求中指定的项目。 当响应`successCount`返回`1`时，操作成功完成。

**请求**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**响应**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

