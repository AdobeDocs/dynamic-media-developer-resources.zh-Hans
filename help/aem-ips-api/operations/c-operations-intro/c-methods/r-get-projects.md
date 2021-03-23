---
description: 获取一组相关资产的项目。
seo-description: 获取一组相关资产的项目。
seo-title: getProjects
solution: Experience Manager
title: getProjects
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 18%

---


# getProjects{#getprojects}

获取一组相关资产的项目。

语法

## 授权用户类型{#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-8d549237b8c440b4872a0a086ddc00a1}

**输入(getProjectsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的手柄。 |

**输出(getProjectsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`projectArray`*` | `types:ProjectArray` | 是 | 与公司关联的项目数组。 |

## 示例 {#section-8b12d0b948f644f68bf9a16060d3849a}

此代码示例返回项目数组中的所有项目句柄。

**请求**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**响应**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

