---
description: 更新晕影发布格式设置。
seo-description: 更新晕影发布格式设置。
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 20%

---


# updateVignettePublishFormat{#updatevignettepublishformat}

更新晕影发布格式设置。

## 授权用户类型{#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-8c7ba8d2bce14071b21fccb11f44749f}

**输入(updateVignettePublishFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 发布格式句柄。 |
| `*`name`*` | `xsd:string` | 否 | 发布格式名称。 |
| `*`targetWidth`*` | `xsd:int` | 是 | 指定生成的晕影目标的视图宽度（以像素为单位）。 使用零，使输出暗角与主暗角大小相同。 |
| `*`targetHeight`*` | `xsd:int` | 是 | 指定所得晕影视图的目标高度（以像素为单位）。 使用零，使输出暗角与主暗角大小相同。 |
| `*`createPyramid`*` | `xsd:boolean` | 是 | 创建为图像渲染服务器上的缩放而优化的金字塔晕影。从通过“目标晕影大小”字段设置的最大大小开始，在单个晕影输出文件中创建多个大小的视图。每个后续视图大小都减半直到宽度和高度在 128x128 像素以内。 |
| `*`thumbWidth`*` | `xsd:int` | 是 | 指定每个生成缩略图的宽度（以像素为单位）。此设置是可选的。 不将缩览图文件保留为零。 |
| `*`saveAsVersion`*` | `xsd:int` | 是 | 指定已发布的晕影的文件格式。 如果具有新版本的图像创作和旧版本的图像渲染服务器，则必须指定ImageRendering Server可以读取的晕影版本。 如果指定更高版本，图像渲染服务器将无法读取已发布的晕影。 设置为零即可在最新版本中发布晕影。 |
| `*`sizeSuffixSeparator`*` | `xsd:string` | 是 | 指定用于分隔晕影名称和后缀（用于指示其宽度）的字符。 |
| `*`锐化`*` | `xsd:int` | 否 | 对每个发布晕影大小的主视图图像应用锐化。缩放晕影时，锐化可以补偿模糊。 |
| `*`usmAmount`*` | `xsd:double` | 是 | 数字USM锐化是一种灵活而强大的方法，可提高锐度，尤其是在扫描的图像中。 这控制每个超调的幅度（边框变暗和变亮的程度）。 |
| `*`usmRadius`*` | `xsd:double` | 是 | 影响要增强的边缘的大小或边缘边缘的宽度，因此，半径越小，细节越小。 半径值越大，边缘处的光晕越多。 细小的细节需要较小的半径，因为大小相同或小于半径的微小细节会丢失。 |
| `*`usmThreshold`*` | `xsd:int` | 是 | 控制要锐化的最小亮度更改或相邻色调值在滤镜工作之前必须相隔的距离。 此设置可锐化更锐化的边缘，同时保持更细微的边缘不变。 阈值的允许范围是0到255。 |

**输出(updateVignettePublishFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 处理更新的晕影发布格式。 |

## 示例 {#section-fcba4bf2b7264786a676e315a35dbe43}

此代码示例更新晕影发布格式并将句柄返回到更新的格式。

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

