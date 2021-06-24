---
description: 获取与图像门户相关的系统属性的字符串值。
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 10%

---

# getProperty{#getproperty}

获取与图像门户相关的系统属性的字符串值。

支持的系统属性包括：

* `IpsVersion`:IPS版本号。
* `IpsImageServerUrl`:IPS图像服务器的完整外部URL前缀。
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`:呈现SVG资产的URL前缀。
* `SvgRenderEnabled`:如果SVG资产可以由呈现，则为 `SvgRenderRootUrl`True。

* `UploadPostMaxFileSize`:上载中允许的文件数据的最大大小（以字节为单位） [!DNL POST]。系统拒绝大于最大限制的文件。

## 授权用户类型 {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**输入(getPropertyParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`name`*` | `xsd:string` | 是 | 要获取的属性的名称。 |

**Output(getPropertyReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`值`*` | `xsd:string` | 是 | 属性值。 |

## 示例 {#section-3f80a78dd60c404181b34d3a912d7a36}

此代码示例使用IPS属性字符串常量返回特定值。 在此示例中，IPS属性是IPS服务器的版本。

**请求**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**响应**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
