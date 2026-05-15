---
description: 创建图像格式。
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
TQID: 'https://experienceleague.adobe.com/kP25DoK-SIRIYh69I8tE07KH4dI-GFZf9JjUZjG-lFw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 10%

---

# saveImageFormat{#saveimageformat}

创建图像格式。

>[!NOTE]
>
>`urlModifier`字段值必须包含有效的XML。 例如，将`&`更改为`&`。 从IPS用户界面获取`urlModfier`值。

## 授权用户类型 {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**输入(saveImageFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 带有您要使用的图像格式的公司句柄。 |
| imageFormatHandle | `xsd:string` | 否 | 要保存的图像格式句柄。 |
| 名称 | `xsd:string` | 是 | 图像格式名称。 |
| urlModifier | `xsd:string` | 是 | 这可以是任何IPS协议查询字符串。 生成URL修饰符的最简单方法是使用IPS用户界面创建一个修饰符，然后剪切并粘贴查询字符串。 |

**输出(saveImageFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | 是 | 处理图像格式。 |

## 示例 {#section-c7bd733212ef494297a97093f3af193f}

此代码示例创建一个图像格式。 在此示例中，`urlModifier`由它在具有有效HTML格式的IPS用户界面中的值决定。

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
