---
description: 图像服务源数据文件包括图像和蒙版文件、字体和ICC配置文件。
solution: Experience Manager
title: 源数据
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# 源数据{#source-data}

图像服务源数据文件包括图像和蒙版文件、字体和ICC配置文件。

所有源数据文件都必须可供图像服务器访问。 图像服务提供了许多指定数据文件位置的替代方法：

`*`install_folder`*/ *`根路径`*/ *`文件路径`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 根路径</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS：：RootPath/attribute：：RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 文件路径 </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|请求路径</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 目录路径</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog：：Path|catalog：：MaskPath|icc：：ProfilePath|font：：FontPath|font：：MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 请求路径</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 图像服务HTTP请求中指定的相对图像文件路径和名称</span> </p></td> 
 </tr> 
</table>

服务器从右到左组合路径区段，直到建立绝对文件路径。

全部 `*`根路径`*` 区段可以是空的、相对或绝对路径区段。

`*`目录路径`*` 是绝对或相对文件路径/名称。 `*`请求路径`*` 必须为相对文件路径/名称。

`Multiple IS::RootPath` 可以在ImageServerRegistry.xml中定义值（或通过管理界面定义）。 这允许跨多个文件系统分发源数据文件。 在找到数据文件之前，图像服务器将按指定的顺序尝试备用路径。

可以随时添加任何类型的新数据文件，而无需停止服务器。
