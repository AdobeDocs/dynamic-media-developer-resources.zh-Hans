---
description: 图像服务源数据文件包括图像和蒙版文件、字体和ICC用户档案。
solution: Experience Manager
title: 源数据
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# 源数据{#source-data}

图像服务源数据文件包括图像和蒙版文件、字体和ICC用户档案。

所有源数据文件都必须可由图像服务器访问。 “图像服务”提供了许多用于指定数据文件位置的备选方案：

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

所有`*`rootPath`*`段都可以是空路径段、相对路径段或绝对路径段。

`*`目`*` 录请选择绝对或相对文件路径/名称。`*`requestPath`*` 必须是相对文件路径/名称。

`Multiple IS::RootPath` 值可在ImageServerRegistry.xml中定义（或通过管理界面定义）。这允许源数据文件跨多个文件系统分发。 图像服务器将按指定顺序尝试替代路径，直到找到数据文件。

可以随时添加任何类型的新数据文件，而无需停止服务器。
