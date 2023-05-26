---
description: 向项目添加一个或多个资产。
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

---

# addProjectAssets{#addprojectassets}

向项目添加一个或多个资产。

语法

## 授权用户类型 {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

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
| companyHandle | `xsd:string` | 是 | 与当前项目关联的公司的句柄。 |
| projectHandle | `xsd:string` | 是 | 处理要向其添加资产的项目。 |
| projectHandlearray | `xsd:HandleArray` | 是 | 要添加到当前项目的资源数组。 |

**输出(addProjectAssetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功添加的资源的数量。 |
| warningCount | `xsd:int` | 是 | 操作尝试将资产添加到项目时生成的警告数。 |
| 错误计数 | `xsd:int` | 是 | 操作尝试将资源添加到项目时生成的错误数。 |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | 否 | 当操作尝试将资源添加到项目时，资源生成的警告数组。 |
| companyHandle | `xsd:AssetOperationFaultArray` | 否 | 当操作尝试将资源添加到项目时，资源生成的错误数组。 |

## 示例 {#section-bee5be2402f54cb9a3a02cc07def4135}

此示例将资产句柄数组中的单个资产（由其句柄引用）添加到请求中指定的项目。 响应时操作成功完成 `successCount` 返回 `1`.

**请求**

```java {.line-numbers}
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**响应**

```java {.line-numbers}
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```
