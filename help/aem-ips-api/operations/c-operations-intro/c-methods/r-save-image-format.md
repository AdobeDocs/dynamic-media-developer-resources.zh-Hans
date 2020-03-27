---
description: 创建图像格式。
seo-description: 创建图像格式。
seo-title: saveImageFormat
solution: Experience Manager
title: saveImageFormat
topic: Scene7 Image Production System API
uuid: b11ea668-7a82-439c-b16b-909dc86c00a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveImageFormat{#saveimageformat}

创建图像格式。

>[!NOTE]
>
>字 `urlModifier` 段值必须由有效的XML组成。 例如，更 `&` 改为 `&`。 从IPS `urlModfier` 用户界面获取值。

## 授权用户类型 {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**输入(saveImageFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司的句柄，其中包含您要处理的图像格式。 |
| ` *`imageFormatHandle`*` | `xsd:string` | 否 | 要保存的图像格式处理。 |
| ` *`名称`*` | `xsd:string` | 是 | 图像格式名称。 |
| ` *`urlModifier`*` | `xsd:string` | 是 | 这可以是任何IPS协议查询字符串。 生成URL修饰符的最简单方法是使用IPS用户界面创建URL修饰符，然后剪切并粘贴查询字符串。 |

**输出(saveImageFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`imageFormatHandle`*` | `xsd:string` | 是 | 处理图像格式。 |

## 示例 {#section-c7bd733212ef494297a97093f3af193f}

此代码范例创建一种图像格式。 在此示例中， `urlModifier` 由IPS用户界面中具有有效HTML格式的值确定。

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

