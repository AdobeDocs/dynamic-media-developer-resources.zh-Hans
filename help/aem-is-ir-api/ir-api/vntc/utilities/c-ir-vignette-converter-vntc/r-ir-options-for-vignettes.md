---
description: 以下选项控制晕影文件的处理。 如果sourceFile不是暗角，则忽略它们。
seo-description: 以下选项控制晕影文件的处理。 如果sourceFile不是暗角，则忽略它们。
seo-title: 晕影选项
solution: Experience Manager
title: 晕影选项
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 晕影选项{#options-for-vignettes}

以下选项控制晕影文件的处理。 如果sourceFile不是暗角，则忽略它们。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -内容</span> </p></td> 
  <td class="stentry"> <p>创建一个表示对象层次结构的XML文件，并包括选定的对象属性。 文件的内容与req=contents命令返回的内 <span class="codeph"> 容相同</span> 。 该文件与源文件同名，但带有 <span class="filepath"> .xml</span> 后缀。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y wid</span><span class="varname"> hei</span><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>在缩放之前裁切暗角。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> 是裁剪矩形的左上角，wid <span class="codeph"><span class="varname"> ,</span>hei<span class="varname"></span></span> 是裁剪矩形的大小。 值是相对于源暗角的全分辨率视图图像的像素坐标。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>在缩放之前裁切暗角。 </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> 是裁剪矩形的左上角，widn <span class="codeph"><span class="varname"> ,</span>hein<span class="varname"></span></span> 是裁剪矩形的大小。 值相对于源暗角的视图图像标准化，且必须介于0.0...1.0之间。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> , <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> 不得大于1.0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -嵌入材料</span> </p></td> 
  <td class="stentry"> <p>将嵌入的材料保留在输出暗角中。 默认情况下，材料会从输出暗角中删除。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>一个或多个输出暗角高度（以像素为单位）。 如果指定-info，则忽略。 <span class="varname"> ival</span> 可以是0，它表示输入暗角的宽度。 有关详 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 细信息，请参阅暗角缩放</a> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>启用提取暗角中的图像映射文件。 映射数据将写入仅包含 <span class="codeph"> &lt;map&gt;元素的HTML文件</span> 。 输出文件的名称与输出图像文件相同，但带有 <span class="filepath"> .htm</span> 后缀。 如果指定命令但暗角中不存在映射数据，则会生成警告消息，并且不会创建文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -配置文件</span> </p></td> 
  <td class="stentry"> <p>将嵌入到暗角中的ICC用户档案的副本保存到文件中。 如果指定命令，但暗角中不存在ICC用户档案，则会生成警告消息，并且不创建ICC用户档案文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -金字塔</span> </p></td> 
  <td class="stentry"> <p>创建金字塔暗角。 在Scene7缩放查看器中显示渲染后的图像时需要。 有关 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 其他信息，请参阅暗角缩放</a> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>缩览图图像的像素宽度和高度限制。 如果指定，则从暗角视图图像、柜样式文件的面板图像或窗口覆盖样式文件中第一样式的照明映射中生成不宽且不高于ival的JPEG图像。 <span class="varname"></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>一个或多个输出暗角宽度（以像素为单位）。 如果指定 <span class="codeph"> -info</span> ，则忽略。 <span class="varname"> ival</span> 可以是0，它表示输入暗角的高度。 有关详 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 细信息，请参阅暗角缩放</a> 。 </p></td> 
 </tr> 
</table>

