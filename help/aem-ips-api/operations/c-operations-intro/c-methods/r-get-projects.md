---
description: 为一组相关资产获取项目。
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: d7262ed7-7419-4d6b-86ed-f3ad4657d654
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 21%

---

# getProjects{#getprojects}

为一组相关资产获取项目。

语法

## 授权用户类型 {#section-337649866b1f4098844d1974ed7ab5d0}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |

**Output(getProjectsReturn)**

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
