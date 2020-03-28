---
description: 创建新项目。
seo-description: 创建新项目。
seo-title: createProject
solution: Experience Manager
title: createProject
topic: Scene7 Image Production System API
uuid: e011b7ba-6c15-47ef-9ea1-6189c37e7719
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createProject{#createproject}

创建新项目。

语法

## 授权用户类型 {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-8c741884eb54489bbaad0c444fee80b6}

**输入(createProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 与新项目关联的公司的句柄。 |
| ` *`projectName`*` | `xsd:string` | 是 | 新项目名称。 |

**输出(createProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`projectHandle`*` | `xsd:string` | 是 | 新项目的句柄。 |

## 示例 {#section-a0cd532b67e346d088fbec141231a0e5}

此代码示例创建一个在由其句柄 `ApiTestProject` 指定的公司中调用的项目。 响应会将句柄返回到项目。

**请求**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```

