---
description: 图像服务源数据文件包括图像和蒙版文件、字体和ICC配置文件。
solution: Experience Manager
title: 源数据
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# 源数据{#source-data}

图像服务源数据文件包括图像和蒙版文件、字体和ICC配置文件。

所有源数据文件必须可供图像服务器访问。 图像服务提供了许多用于指定数据文件位置的替代方法：

`*`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 在图像服务HTTP请求中指定的相对图像文件路径和名称</span> </p></td> 
 </tr> 
</table>

服务器从右到左组合路径段，直到建立绝对文件路径。

所有`*`rootPath`*`区段都可以是空、相对或绝对路径区段。

`*``*` catalog（目录）以绝对或相对文件路径/名称分配。`*``*` requestPath必须是相对文件路径/名称。

`Multiple IS::RootPath` 值可在ImageServerRegistry.xml中定义（或通过管理界面定义）。这允许源数据文件跨多个文件系统分发。 图像服务器将尝试按照指定的顺序使用替代路径，直到找到数据文件为止。

任何类型的新数据文件都可以随时添加，而无需停止服务器。
