---
description: 图像服务源数据文件包括图像和蒙版文件、字体和ICC用户档案。
seo-description: 图像服务源数据文件包括图像和蒙版文件、字体和ICC用户档案。
seo-title: 源数据
solution: Experience Manager
title: 源数据
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 源数据{#source-data}

图像服务源数据文件包括图像和蒙版文件、字体和ICC用户档案。

所有源数据文件都必须可由图像服务器访问。 图像服务提供了许多用于指定数据文件位置的备选方案：

` *`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 根 <span class="varname"> 路径</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> file <span class="varname"> Path </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog <span class="varname"> Path</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> requestPath(请 <span class="varname"> 求路径)</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 在图像服务HTTP请求中指定的相对图像文件路径和名称</span> </p></td> 
 </tr> 
</table>

服务器从右到左组合路径段，直到建立绝对文件路径。

所有 ` *`rootPath段`*` （相对路径段或绝对路径段）可以是空的。

` *`catalogPath是`*` absolute或relative file path/name。 ` *`requestPath必须是`*` 相对文件路径／名称。

`Multiple IS::RootPath` 可以在ImageServerRegistry.xml中定义值（或通过管理界面）。 这允许在多个文件系统中分发源数据文件。 图像服务器将按指定的顺序尝试替代路径，直到找到数据文件。

可以随时添加任何类型的新数据文件而无需停止服务器。
