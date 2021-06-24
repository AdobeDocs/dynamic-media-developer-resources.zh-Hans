---
description: 更新晕影发布格式设置。
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 20%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

更新晕影发布格式设置。

## 授权用户类型 {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-8c7ba8d2bce14071b21fccb11f44749f}

**输入(updateVignettePublishFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司负责人。 |
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 发布格式句柄。 |
| `*`name`*` | `xsd:string` | 否 | 发布格式名称。 |
| `*`targetWidth`*` | `xsd:int` | 是 | 以像素为单位指定所生成晕影视图的目标宽度。 使用零，使输出晕影与主晕影大小相同。 |
| `*`targetHeight`*` | `xsd:int` | 是 | 以像素为单位指定所生成晕影视图的目标高度。 使用零，使输出晕影与主晕影大小相同。 |
| `*`createPyramid`*` | `xsd:boolean` | 是 | 创建为图像渲染服务器上的缩放而优化的金字塔晕影。从通过“目标晕影大小”字段设置的最大大小开始，在单个晕影输出文件中创建多个大小的视图。每个后续视图大小都减半直到宽度和高度在 128x128 像素以内。 |
| `*`thumbWidth`*` | `xsd:int` | 是 | 指定每个生成缩略图的宽度（以像素为单位）。此设置是可选的。 不将缩略图文件保留为零。 |
| `*`saveAsVersion`*` | `xsd:int` | 是 | 指定已发布的小图的文件格式。 如果提供了图像创作的新版本和图像渲染服务器的早期版本，则必须指定图像渲染服务器可以读取的晕影版本。 如果指定更高版本，则图像渲染服务器将无法读取已发布的晕影。 若要在最新版本中发布小图，则设置为0。 |
| `*`sizeSuffixSeparator`*` | `xsd:string` | 是 | 指定用于分隔晕影名称和后缀（用于指示其宽度）的字符。 |
| `*`锐化`*` | `xsd:int` | 否 | 对每个发布晕影大小的主视图图像应用锐化。缩放晕影时，锐化可以补偿模糊。 |
| `*`usmAmount`*` | `xsd:double` | 是 | 数字USM锐化是一种灵活且功能强大的方法，可提高锐度，尤其是在扫描的图像中。 这控制每个超调量的大小（边界变得更暗和更亮的程度）。 |
| `*`usmRadius`*` | `xsd:double` | 是 | 影响要增强的边缘的大小或边缘边缘的宽度，因此半径越小，细节越小。 半径值越大，边缘处的光晕就越多。 细小细节需要较小的半径，因为丢失大小相同或小于半径的细小细节。 |
| `*`usmThreshold`*` | `xsd:int` | 是 | 控制要锐化的最小亮度更改或相邻色调值在滤镜工作之前必须相距的距离。 此设置可锐化更突出的边缘，同时保持更细微的边缘不变。 允许的阈值范围为0到255。 |

**Output(updateVignettePublishFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 处理更新的晕影发布格式。 |

## 示例 {#section-fcba4bf2b7264786a676e315a35dbe43}

此代码示例会更新晕影发布格式，并将句柄返回为更新的格式。

**请求**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**响应**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```
