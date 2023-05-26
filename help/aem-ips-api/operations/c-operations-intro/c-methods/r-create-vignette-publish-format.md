---
description: 为晕影创建新的发布格式。
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 5%

---

# createVignettePublishFormat{#createvignettepublishformat}

为晕影创建新的发布格式。

晕影格式指定已发布晕影及其缩略图的大小，以及缩放级别、锐化参数和从IPS发布到图像渲染服务器的主晕影生成的晕影的文件格式版本。

较新的图像渲染服务器版本可以支持金字塔晕影，从而无需为发布定义特定的晕影格式大小。

## 授权用户类型 {#section-f5c563e3695c4dba8df41e2a965aace7}

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
   <td colname="col4"> 处理晕影所属的公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 用于标识晕影发布格式的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetwidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>指定生成的晕影视图的目标宽度（以像素为单位）。 </p> <p>使用零以使输出晕影具有与主晕影相同的大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 创建为图像渲染服务器上的缩放而优化的金字塔晕影。 从“目标晕影大小”字段设置的最大大小开始，这会在单个晕影输出文件中创建多个大小视图。 每个后续视图大小都会减半，直到宽度和高度在128x128像素以内。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定每个结果缩略图的宽度（像素）。 此设置是可选的。 对于无缩略图文件，保留为0。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 缩略图宽度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定已发布晕影的文件格式。 给定图像创作的新版本和图像渲染服务器的旧版本，您必须指定图像渲染服务器可以读取的晕影版本。 如果指定更高版本，则图像渲染服务器无法读取已发布的晕影。 设置为零可发布最新版本的晕影。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定用于分隔晕影名称和后缀（用于指示其宽度）的字符。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 指定用于分隔晕影名称和后缀（用于指示其宽度）的字符。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 锐化</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 对每个发布的晕影大小的主视图图像应用锐化。锐化可在缩放晕影时补偿模糊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 数字钝化蒙版是一种灵活而强大的提高锐度的方法，尤其是在扫描的图像中。 这控制了每次超调的幅度（边缘边界变得多暗多亮）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影响要增强的边的大小或边框的宽度，因此较小的半径可增强小尺度细节。 较高的半径值可能会导致边缘出现光晕。 精细细节需要较小的半径，因为大小相同或小于该半径的微小细节会丢失。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 控制要锐化的最小亮度变化或在滤镜工作之前相邻色调值必须相距多远。 此设置可以锐化更细微的边缘，同时保持更细微的边缘不变。 阈值允许范围为0到255。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(createVignettePublishFormatReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | 是 | 创建的晕影格式的句柄。 |

## 示例 {#section-0564752d439642b9bb8de2903db6de1e}

此代码创建晕影发布格式。 创建请求会指定名称、目标宽度和高度以及其他必需值。

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
