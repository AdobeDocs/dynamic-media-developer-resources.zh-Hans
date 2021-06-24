---
description: 创建图像格式。
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 11%

---

# saveImageFormat{#saveimageformat}

创建图像格式。

>[!NOTE]
>
>`urlModifier`字段值必须由有效的XML组成。 例如，将`&`更改为`&`。 从IPS用户界面获取`urlModfier`值。

## 授权用户类型 {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**输入(saveImageFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含您要处理的图像格式的公司句柄。 |
| `*`imageFormatHandle`*` | `xsd:string` | 否 | 要保存的图像格式句柄。 |
| `*`name`*` | `xsd:string` | 是 | 图像格式名称。 |
| `*`urlModifier`*` | `xsd:string` | 是 | 这可以是任何IPS协议查询字符串。 生成URL修饰符的最简单方法是使用IPS用户界面创建一个，然后剪切并粘贴查询字符串。 |

**输出(saveImageFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`imageFormatHandle`*` | `xsd:string` | 是 | 处理图像格式。 |

## 示例 {#section-c7bd733212ef494297a97093f3af193f}

此代码示例创建图像格式。 在此示例中，`urlModifier`由IPS用户界面中具有有效HTML格式的值决定。

**请求**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**响应**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```
