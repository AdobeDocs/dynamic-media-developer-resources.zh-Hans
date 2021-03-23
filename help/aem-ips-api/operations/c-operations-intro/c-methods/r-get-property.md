---
description: 获取与图像门户相关的系统属性的字符串值。
seo-description: 获取与图像门户相关的系统属性的字符串值。
seo-title: getProperty
solution: Experience Manager
title: getProperty
uuid: 38ea08a6-c948-4a01-bc9a-d1609197224e
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 10%

---


# getProperty{#getproperty}

获取与图像门户相关的系统属性的字符串值。

支持的系统属性包括：

* `IpsVersion`:IPS版本号。
* `IpsImageServerUrl`:IPS图像服务器的完整外部URL前缀。
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`:用于呈现SVG资源的URL前缀。
* `SvgRenderEnabled`:如果SVG资源可以由渲染器呈 `SvgRenderRootUrl`现。

* `UploadPostMaxFileSize`:上载中允许的文件数据的最大大小（以字节为单位）  [!DNL POST]。系统拒绝大于最大限制的文件。

## 授权用户类型{#section-2cd36bbd46ed414b8753569d5895530e}

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

**Input(getPropertyParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`name`*` | `xsd:string` | 是 | 要获取的属性的名称。 |

**输出(getPropertyReturn)**

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

