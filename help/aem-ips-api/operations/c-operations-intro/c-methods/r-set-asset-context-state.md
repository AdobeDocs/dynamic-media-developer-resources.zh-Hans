---
description: 为一个或多个资产设置或更新发布状态。 您可以在公司中为每个发布上下文设置单独的发布状态。
seo-description: 为一个或多个资产设置或更新发布状态。 您可以在公司中为每个发布上下文设置单独的发布状态。
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
topic: Dynamic Media Image Production System API
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 9%

---


# setAssetsContextState{#setassetscontextstate}

为一个或多个资产设置或更新发布状态。 您可以在公司中为每个发布上下文设置单独的发布状态。

## 授权用户类型{#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有读取权限才能返回资产。

## 参数 {#section-009b9006de8e4c16ad657c47f28ace9f}

**输入(setAssetsContextStateParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | 是 | 一组资源及其新发布状态。 |

**输出(setAssetsContexStateReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功更改的资产数。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试修改资产时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试修改资产时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 资产在操作尝试修改资产时生成的错误数组。 |

## 示例 {#section-283a073f3cb14bcda5abed863c538aa4}

此代码示例使用`NotMarkedForPublish`设置资产的发布状态。

**请求**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**响应**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```

