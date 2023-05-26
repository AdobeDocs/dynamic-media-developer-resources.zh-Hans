---
description: 以下选项控制晕影文件的处理。 如果sourceFile不是晕影，则会忽略它们。
solution: Experience Manager
title: 晕影选项
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 晕影选项{#options-for-vignettes}

以下选项控制晕影文件的处理。 如果sourceFile不是晕影，则会忽略它们。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -内容</span> </p></td> 
  <td class="stentry"> <p>创建表示对象层次结构的XML文件，包括所选对象属性。 文件的内容与 <span class="codeph"> req=contents</span> 命令。 该文件与源文件同名，但使用 <span class="filepath"> .xml</span> 后缀。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>缩放之前裁切晕影。 </p> <p><span class="codeph"><span class="varname"> x</span>，<span class="varname"> y</span></span> 是裁切矩形的左上角，并且 <span class="codeph"><span class="varname"> wid</span>，<span class="varname"> hei</span></span> 是裁切矩形的大小。 值是相对于源晕影的全分辨率视图图像的像素坐标。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> 宽度</span><span class="varname"> 海因</span></span> </p> </td> 
  <td class="stentry"> <p>缩放之前裁切晕影。 </p> <p><span class="codeph"><span class="varname"> xn</span>，<span class="varname"> yn</span></span> 是裁切矩形的左上角，并且 <span class="codeph"><span class="varname"> 宽度</span>，<span class="varname"> 海因</span></span> 是裁切矩形的大小。 该值相对于源晕影的视图图像进行规范化，且必须介于0.0...1.0之间。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> 宽度</span></span> 和 <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> 海因</span></span> 不得大于1.0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — 嵌入材料</span> </p></td> 
  <td class="stentry"> <p>将嵌入的材料保留在输出晕影中。 默认情况下，材料会从输出晕影中删除。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>一个或多个输出晕影高度（以像素为单位）。 如果指定了 — info，则忽略。 <span class="varname"> ival</span> 可以为0，表示输入晕影的宽度。 参见 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 晕影缩放</a> 以了解详细信息。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>启用从晕影中提取图像映射文件。 HTML映射数据将写入一个仅包含 <span class="codeph"> &lt;map&gt;</span> 元素。 输出文件的名称与输出图像文件的名称相同，但使用 <span class="filepath"> .htm</span> 后缀。 如果指定了命令但晕影中不存在映射数据，则会生成警告消息，并且不会创建文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -配置文件</span> </p></td> 
  <td class="stentry"> <p>将晕影中嵌入的ICC配置文件副本保存到文件。 如果指定命令但晕影中不存在ICC配置文件，则会生成警告消息，并且不创建ICC配置文件文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — 金字塔</span> </p></td> 
  <td class="stentry"> <p>创建金字塔晕影。 在渲染的图像将使用Dynamic Media缩放查看器显示时必需。 参见 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 晕影缩放</a> 以获取其他信息。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 缩略图 <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>缩略图图像的像素宽度和高度限制。 如果指定，则JPEG图像不宽也不高 <span class="varname"> ival</span> 从晕影视图图像、文件柜样式文件的面板图像或窗口覆盖样式文件中的第一个样式的照明地图生成。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[，<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>一个或多个输出晕影宽度（像素）。 忽略条件 <span class="codeph"> -info</span> 已指定。 <span class="varname"> ival</span> 可以为0，表示输入晕影的高度。 参见 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 晕影缩放</a> 以了解详细信息。 </p></td> 
 </tr> 
</table>
