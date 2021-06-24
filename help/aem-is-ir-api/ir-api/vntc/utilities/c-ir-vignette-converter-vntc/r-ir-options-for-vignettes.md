---
description: 以下选项控制晕影文件的处理。 如果sourceFile不是晕影，则忽略它们。
solution: Experience Manager
title: 晕影选项
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# 晕影选项{#options-for-vignettes}

以下选项控制晕影文件的处理。 如果sourceFile不是晕影，则忽略它们。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -内容</span> </p></td> 
  <td class="stentry"> <p>创建表示对象层次结构并包括所选对象属性的XML文件。 文件内容与<span class="codeph"> req=contents</span>命令返回的内容相同。 文件与源文件同名，但后缀为<span class="filepath"> .xml</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 农作物 <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> 木</span></span> </p></td> 
  <td class="stentry"> <p>在缩放前裁剪晕影。 </p> <p><span class="codeph"><span class="varname"> x</span>、<span class="varname"> </span></span> 是裁剪矩形的左上角， <span class="codeph"><span class="varname"> wid</span>、<span class="varname"> </span></span> 是裁剪矩形的大小。值是相对于源晕影的全分辨率视图图像的像素坐标。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn xnynwidnhein <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> </span></span> </p> </td> 
  <td class="stentry"> <p>在缩放前裁剪晕影。 </p> <p><span class="codeph"><span class="varname"> xn</span>、<span class="varname"> </span></span> yn是裁剪矩形的左上角， <span class="codeph"><span class="varname"> widn</span>和<span class="varname"> </span></span> hein是裁剪矩形的大小。值是相对于源晕影的视图图像进行标准化的，且必须介于0.0..1.0之间。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> hein不得大于1.0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 埋藏材料</span> </p></td> 
  <td class="stentry"> <p>在输出晕影中保留嵌入的材料。 默认情况下，将从输出晕影中移除材料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>一个或多个输出晕影高度（以像素为单位）。 如果指定了 — info，则忽略。 <span class="varname"> </span> 值可以为0，表示输入晕影的宽度。有关详细信息，请参阅<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">晕影缩放</a> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>允许从晕影中提取图像映射文件。 映射数据将写入仅包含<span class="codeph"> &lt;map&gt;</span>元素的HTML文件。 输出文件的名称与输出图像文件相同，但带有<span class="filepath"> .htm</span>后缀。 如果指定了命令，但晕影中没有映射数据，则会生成警告消息，并且不会创建文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -配置文件</span> </p></td> 
  <td class="stentry"> <p>将嵌入到晕影中的ICC配置文件的副本保存到文件。 如果指定了命令，但晕影中不存在ICC配置文件，则会生成警告消息，并且不会创建ICC配置文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — 金字塔</span> </p></td> 
  <td class="stentry"> <p>创建金字塔晕影。 使用Dynamic Media缩放查看器显示渲染的图像时需要此参数。 有关其他信息，请参阅<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">晕影缩放</a> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>缩略图像的像素宽度和高度约束。 如果指定，则从晕影视图图像、柜式文件的面板图像或窗口覆盖样式文件中第一样式的照明映射中生成不大于<span class="varname"> ival</span>的JPEG图像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>一个或多个输出晕影宽度（以像素为单位）。 如果指定了<span class="codeph"> -info</span>，则忽略。 <span class="varname"> </span> 值可以为0，表示输入晕影的高度。有关详细信息，请参阅<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">晕影缩放</a> 。 </p></td> 
 </tr> 
</table>
