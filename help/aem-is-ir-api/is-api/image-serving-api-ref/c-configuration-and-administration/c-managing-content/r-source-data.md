---
description: 图像服务源数据文件包括图像和蒙版文件、字体和ICC配置文件。
solution: Experience Manager
title: Source数据
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Source数据{#source-data}

图像服务源数据文件包括图像和蒙版文件、字体和ICC配置文件。

所有源数据文件都必须可供图像服务器访问。 图像服务提供了许多指定数据文件位置的替代方法：

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">根路径</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS：：RootPath/attribute：：RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">文件路径</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">目录路径</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog：：Path|catalog：：MaskPath|icc：：ProfilePath|font：：FontPath|font：：MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">请求路径</span></span> </p></td> 
  <td class="stentry"> <p>在图像服务HTTP请求中指定的<span class="codeph">相对图像文件路径和名称</span> </p></td> 
 </tr> 
</table>

服务器将从右到左组合路径段，直到建立绝对文件路径。

所有`*`rootPath`*`区段都可为空、相对或绝对路径区段。

`*`catalogPath`*`是绝对或相对文件路径/名称。 `*`requestPath`*`必须为相对的文件路径/名称。

可以在ImageServerRegistry.xml中定义`Multiple IS::RootPath`值（或通过管理接口）。 这允许跨多个文件系统分发源数据文件。 图像服务器将按指定的顺序尝试备用路径，直到找到数据文件为止。

任何类型的新数据文件都可以随时添加，而无需停止服务器。
