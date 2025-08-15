---
description: vntc生成文本数据，该数据将发送到stderr或日志文件。
solution: Experience Manager
title: 输出
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# 输出{#output}

vntc生成文本数据，该数据将发送到stderr或日志文件。

每个文本记录的数据格式为一个`name=value`属性。 字符串值未加引号。 警告和错误消息始终发送到`stderr`，即使指定了`-log`也是如此。

某些属性可能会在同一输出中多次出现。 以0开头的序列号将附加到这些属性的名称中，并以句点分隔。 此类属性在属性名称后面有`. *`n`*`后缀。

将生成以下属性：

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>，<span class="varname"> ival</span>，<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>机柜样式的RGB背景色。 仅限文件柜样式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>默认输出文件版本。 另外，此版本的<span class="filepath"> vntc</span>可以生成的最高文件版本号。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">错误。<span class="varname"> n</span>=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>错误消息。 如果存在错误消息，则通常表示未创建输出文件，或者输出文件不适合由图像渲染使用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">文件。<span class="varname"> n</span>=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>所有输出文件（包括晕影、文件柜样式文件、全分辨率图像和缩略图图像）的完全限定的路径/名称。 每个生成的文件（日志文件除外）都存在一个文件属性。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">玻璃=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果机柜包含玻璃门，则<span class="varname"> ival</span>为1，否则为0。 仅限文件柜样式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>嵌入到<span class="varname"> sourceFile</span>中的iccProfile的名称。 </p> <p>如果<span class="varname"> sourceFile</span>不是颜色管理的，则为空。 仅晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">信息。<span class="varname"> n</span>=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>信息性消息，如进度信息。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果<span class="varname"> sourceFile</span>是主晕影，则<span class="varname"> ival</span>为1；如果之前已使用<span class="filepath"> vnUpdate</span>或<span class="filepath"> vntc</span>处理了该晕影，则为0。 仅晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果<span class="varname"> sourceFile</span>是包含JPEG图像数据的文件柜样式（在这种情况下，也会输出警告），则<span class="varname"> ival</span>为0，否则为1。 仅用于文件柜和窗口覆盖样式文件。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>适用于正在运行的<span class="filepath"> vntc</span>进程的最大内存限制。 <span class="varname">字符串</span>为<span class="varname"> ival</span>、<span class="varname"> ivalK</span>、<span class="varname"> ivalM</span>、<span class="varname"> ivalG</span>或<span class="codeph"> 0</span>（已禁用）。 其中<span class="varname"> K</span>、<span class="varname"> M</span>和<span class="varname"> G</span>指的是KB （1024字节）、MB (1048576字节)和GB (1073741824字节)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>输出晕影中分辨率最低的金字塔级别的比例。 仅在指定<span class="codeph"> -pyramid</span>时存在。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>中保存的材料数。 仅晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>此CAB样式文件中的面板图像数。 仅限文件柜样式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>输出晕影中的金字塔级别数。 仅在指定 — pyramid时存在。 仅晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">金字塔=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果源或目标晕影具有金字塔结构，则为0。 仅晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">分辨率=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>对于文件柜样式，<span class="varname"> sourceFile</span>的对象分辨率。 对于晕影，在渲染输出晕影时，为获得最佳质量的渲染结果，建议使用此材料分辨率。 像素/英寸(ppi)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>输出晕影中最小的对象分辨率。 仅晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>输出晕影中的平均对象分辨率。 仅晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>完全限定的<span class="varname">源文件</span>路径。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>的文件版本。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>，<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>输入晕影、文件柜样式文件中的默认面板图像或窗口覆盖样式文件中的第一个不透明度图像的像素大小。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>窗饰的类型（仅限窗饰样式）： </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=水平阴影或百叶窗 </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直百叶窗 </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全宽短窗帘 </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左/右短窗帘 </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全宽全长窗帘 </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左/右全长窗帘 </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=咖啡馆窗帘 </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=瓦朗斯 </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>如果<span class="codeph"> sourceFile</span>是晕影，则为<span class="varname"> vnt</span>；如果<span class="codeph"> sourceFile</span>是封包样式，则为<span class="varname"> vnc</span>；如果<span class="codeph"> sourceFile</span>是窗口覆盖样式，则为<span class="varname"> vnw</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>使用<span class="codeph"> -version</span>指定的值，或者如果未指定<span class="codeph"> -version</span>，则使用<span class="codeph"> defaultFileVersion</span>的值。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>，<span class="varname"> ival</span>*[，<span class="varname"> ival</span>，<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>以逗号分隔的输出晕影（金字塔晕影的全分辨率视图）中所有视图、文件柜样式文件中的默认面板图像或窗口覆盖样式文件的第一个不透明度图像的像素大小列表。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果文件柜样式是可纹理的，则<span class="varname"> ival</span>为1，否则为0。 对于晕影和窗口覆盖样式文件不存在。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告。<span class="varname"> n</span>=<span class="varname">字符串</span></span> </p></td> 
  <td class="stentry"> <p>警告消息（例如，当指定了<span class="codeph"> -imagemap</span>，但在晕影中未找到映射数据时）。 </p></td> 
 </tr> 
</table>
