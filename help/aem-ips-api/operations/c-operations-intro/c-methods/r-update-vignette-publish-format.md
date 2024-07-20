---
description: 更新晕影发布格式设置。
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 5%

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
| companyHandle | `xsd:string` | 是 | 公司句柄。 |
| vignetteFormatHandle | `xsd:string` | 是 | Publish格式句柄。 |
| 名称 | `xsd:string` | 否 | Publish格式名称。 |
| targetwidth | `xsd:int` | 是 | 指定生成的晕影视图的目标宽度（以像素为单位）。 使用零以使输出晕影具有与主晕影相同的大小。 |
| targetHeight | `xsd:int` | 是 | 指定生成的晕影视图的目标高度（以像素为单位）。 使用零以使输出晕影具有与主晕影相同的大小。 |
| createPyramid | `xsd:boolean` | 是 | 创建为图像渲染服务器上的缩放而优化的金字塔晕影。 从目标晕影大小字段设置的最大大小开始，这会在单个晕影输出文件中创建多个大小视图。 每个后续视图大小都减半，直到宽度和高度在128x128像素以内。 |
| 缩略图宽度 | `xsd:int` | 是 | 指定每个结果缩略图的宽度（像素）。 此设置是可选的。 对于无缩略图文件，保留为0。 |
| saveAsVersion | `xsd:int` | 是 | 指定已发布晕影的文件格式。 给定图像创作的新版本和图像渲染服务器的旧版本，必须指定您的图像渲染服务器可以读取的晕影版本。 如果指定较高的版本，则图像渲染服务器无法读取发布的晕影。 设置为零可发布最新版本的晕影。 |
| sizeSuffixSeparator | `xsd:string` | 是 | 指定用于分隔晕影名称和后缀（用于指示其宽度）的字符。 |
| 锐化 | `xsd:int` | 否 | 对每个发布晕影大小的主视图图像应用锐化。 锐化可在缩放晕影时补偿模糊。 |
| usmAmount | `xsd:double` | 是 | 数字钝化蒙版是一种灵活而强大的增强锐度的方法，尤其是在扫描的图像中。 这控制每个超调的大小（边缘边框变得多深多浅）。 |
| usmRadius | `xsd:double` | 是 | 影响要增强的边的大小或边框变得多宽，因此较小的半径可增强更小的细节。 半径值越大，边缘会出现光晕。 细细节需要较小的半径，因为与半径相同或小于该半径的微小细节将丢失。 |
| usmThreshold | `xsd:int` | 是 | 控制要锐化的最小亮度变化或在滤镜工作之前相邻色调值必须相距多远。 此设置可以锐化更细微的边缘，同时保持更细微的边缘不变。 阈值允许范围为0到255。 |

**输出(updateVignettePublishFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | 是 | 处理更新的晕影发布格式。 |

## 示例 {#section-fcba4bf2b7264786a676e315a35dbe43}

此代码示例更新晕影发布格式，并将句柄返回到更新的格式。

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
