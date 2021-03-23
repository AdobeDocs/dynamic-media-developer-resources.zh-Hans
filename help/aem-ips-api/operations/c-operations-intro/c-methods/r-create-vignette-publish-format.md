---
description: 为晕影创建新的发布格式。
seo-description: 为晕影创建新的发布格式。
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
uuid: 834ebe6a-e105-4075-8004-172237980933
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 14%

---


# createVignettePublishFormat{#createvignettepublishformat}

为晕影创建新的发布格式。

晕影格式指定已发布的晕影及其缩览图的大小，以及缩放级别、锐化参数以及从IPS发布到图像渲染服务器的主晕影生成的晕影的文件格式版本。

较新的图像渲染服务器版本可支持金字塔晕影，这消除了为发布定义特定晕影格式大小的需求。

## 授权用户类型{#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-3a368186ec1d4005bca056fc9d9bacc7}

**输入(createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 晕影所属的公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 用于标识晕影发布格式的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>指定生成的晕影目标的视图宽度（以像素为单位）。 </p> <p>使用零，使输出暗角与主暗角大小相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 创建为图像渲染服务器上的缩放而优化的金字塔晕影。从通过“目标晕影大小”字段设置的最大大小开始，在单个晕影输出文件中创建多个大小的视图。每个后续视图大小都减半直到宽度和高度在 128x128 像素以内。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定每个生成缩略图的宽度（以像素为单位）。此设置是可选的。 不将缩览图文件保留为零。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定已发布的晕影的文件格式。 如果提供了新版本的图像创作和旧版本的图像渲染服务器，则必须指定ImageRendering Server可以读取的晕影版本。 如果指定更高版本，图像渲染服务器将无法读取已发布的晕影。 设置为零即可在最新版本中发布晕影。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔晕影名称和指示其宽度的后缀的字符。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定分隔晕影名称和指示其宽度的后缀的字符。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 锐化</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 将锐化应用于每个小晕影大小的主视图图像锐化可补偿缩放晕影时的模糊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 数字USM锐化是一种灵活而强大的方法，可提高锐度，尤其是在扫描的图像中。 这控制每个超调量（边框变暗和变亮的程度）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影响要增强的边缘的大小或边缘边缘的宽度，因此较小的半径会增强较小的细节。 半径值越大，边缘处的光晕越多。 细小的细节需要较小的半径，因为大小相同或小于半径的微小细节会丢失。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 控制要锐化的最小亮度更改或相邻色调值在滤镜工作之前必须相隔的距离。 此设置可锐化更锐化的边缘，同时保持更细微的边缘不变。 阈值的允许范围是0到255。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(createVignettePublishFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 创建晕影格式的句柄。 |

## 示例 {#section-0564752d439642b9bb8de2903db6de1e}

此代码创建晕影发布格式。 创建请求指定名称、目标宽度和高度以及其他必需值。

**请求**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**响应**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```

