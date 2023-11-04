---
description: 替换图像资源的图像数据。
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 16%

---

# replaceImage{#replaceimage}

替换图像资源的图像数据。

语法

## 授权用户类型 {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**输入(replaceImageParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyName | `xsd:string` | 是 | 带有要替换的图像的公司的句柄。 |
| assetHandle | `xsd:string` | 是 | 要替换的资源的句柄。 |
| urlModifier | `xsd:string` | 是 | 生成新图像数据的图像服务器命令。 |

**输出(replaceImageReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 处理新资源。 |

## 示例 {#section-cebb93576bde4cb98cb27356ca66783b}

此代码示例替换图像并应用 `urlModifier` 使用指定图像服务器不执行替换操作的命令。

**请求**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**响应**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```
