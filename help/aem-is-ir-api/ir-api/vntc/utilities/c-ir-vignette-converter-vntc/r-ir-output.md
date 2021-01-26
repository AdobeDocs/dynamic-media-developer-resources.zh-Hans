---
description: vntc生成文本数据，该数据被发送到stderr或日志文件。
seo-description: vntc生成文本数据，该数据被发送到stderr或日志文件。
seo-title: 输出
solution: Experience Manager
title: 输出
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# 输出{#output}

vntc生成文本数据，该数据被发送到stderr或日志文件。

数据的格式为每个文本记录的一个`name=value`属性。 字符串值不加引号。 警告和错误消息始终发送到`stderr`，即使指定了`-log`。

某些属性可能在同一输出中多次发生。 从0开始的序列号将附加到这些属性的名称中，以句点分隔。 这些属性在下面以`. *`n`*`后缀标识。

将生成以下属性：

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span><span class="varname"> ,ival</span></span> </p> </td> 
  <td class="stentry"> <p>机柜样式的RGB背景颜色。 仅限文件柜样式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>默认输出文件版本。 此版本<span class="filepath"> vntc</span>可生成的最高文件版本号。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">错误.<span class="varname"> n</span>=字<span class="varname"> 符串</span></span> </p></td> 
  <td class="stentry"> <p>错误消息. 出现错误消息通常表示未创建输出文件，或者它们不适合由图像渲染使用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">文件。<span class="varname"> n</span>=字<span class="varname"> 符串</span></span> </p></td> 
  <td class="stentry"> <p>所有输出文件（包括晕影、文件柜样式文件、全分辨率图像和缩略图图像）的完全限定路径／名称。 每个生成的文件（日志文件除外）都有一个文件属性。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 如</span> 果机柜包括玻璃门，则为ivalis 1，否则为0。仅限文件柜样式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>嵌入在<span class="varname"> sourceFile</span>中的iccProfile的名称。 </p> <p>如果<span class="varname"> sourceFile</span>未进行颜色管理，则为空。 仅限晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=字<span class="varname"> 符串</span></span> </p></td> 
  <td class="stentry"> <p>信息性消息，如进度信息。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 如</span> 果sourceFile是主控 <span class="varname"> </span> 暗角，则为ivalis 1；如果它先前已使用vnUpdate或vntc <span class="filepath"> </span> 处理，则 <span class="filepath"> 为0</span>。仅限晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">主控=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 如</span> 果sourceFile是包 <span class="varname"> </span> 含JPEG图像数据的文件柜样式（在这种情况下也会输出警告），则为ivalis 0，否则为1。仅覆盖样式文件的文件柜和窗口。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>运行的<span class="filepath"> vntc</span>进程所适用的最大内存限制。 <span class="varname"> </span> stringis  <span class="varname"> ival</span>K、 <span class="varname"> ivalM</span>、 <span class="varname"> ival</span> G <span class="varname"> </span> <span class="codeph"> </span> 、或（禁用）。其中<span class="varname"> K</span>、<span class="varname"> M</span>和<span class="varname"> G</span>指的是千字节（1024字节）、兆字节（1048576字节）和千兆字节（1073741824字节）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>输出暗角中最低分辨率金字塔级的比例。 仅当指定<span class="codeph"> -pyramid</span>时存在。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>保存在<span class="varname"> sourceFile</span>中的材料数。 仅限晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>此文件柜样式文件中的面板图像数。 仅限文件柜样式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>输出暗角中的金字塔级数。 仅当指定了-pyramid时才存在。 仅限晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">金字塔=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果源暗角或目标暗角具有金字塔结构，则为0。 仅限晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>对于文件柜样式，<span class="varname"> sourceFile</span>的对象分辨率。 对于晕影，这是在渲染输出暗角时为获得最佳质量渲染结果而推荐的材料分辨率。 像素／英寸(ppi)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>输出暗角中最小的对象分辨率。 仅限晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>输出暗角中的平均对象分辨率。 仅限晕影。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>完全限定的<span class="varname"> sourceFile</span>路径。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>的文件版本。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>输入暗角的像素大小、文件柜样式文件中的默认面板图像或窗口覆盖样式文件中的第一个不透明度图像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>窗口覆盖类型（仅限窗口覆盖样式）: </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=水平阴影或百叶窗 </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直百叶窗 </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全宽短窗帘 </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左／右短窗帘 </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全宽全长窗帘 </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左／右全长窗帘 </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6.咖啡帘 </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vntif </span> sourceFile <span class="varname"> </span> 是暗角， <span class="codeph"> </span> vncif sourceFile是 <span class="varname"> </span> 文件柜样式，或vnwif sourceFile是 <span class="codeph"> </span> 一 <span class="varname"> </span> 个覆盖样式的窗口。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>用<span class="codeph"> -version</span>指定的值，或者如果未指定<span class="codeph"> -version</span>，则使用<span class="codeph"> defaultFileVersion</span>指定的值。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span><span class="varname"> ,</span>ival<span class="varname"> *[,</span>ival<span class="varname"> ,</span>ival ]</span> </p></td> 
  <td class="stentry"> <p>输出暗角中所有视图的像素大小(金字塔暗角的全分辨率视图)、文件柜样式文件中默认面板图像或窗口覆盖样式文件中第一个不透明度图像的列表以逗号分隔。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 如</span> 果机柜样式可纹理化，则为ivalis 1，否则为0。晕影和窗口覆盖样式文件不存在。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告.<span class="varname"> n</span>=字<span class="varname"> 符串</span></span> </p></td> 
  <td class="stentry"> <p>警告消息（例如，当指定<span class="codeph"> -imagemap</span>但在暗角中找不到映射数据时）。 </p></td> 
 </tr> 
</table>

