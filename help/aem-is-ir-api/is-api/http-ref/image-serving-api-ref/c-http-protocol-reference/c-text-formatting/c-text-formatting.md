---
description: 图像服务提供了几种呈现文本的替代方法，使用text=和textPs=命令可访问这些方法。
solution: Experience Manager
title: 文本格式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 6%

---

# 文本格式{#text-formatting}

图像服务提供了几种呈现文本的替代方法，使用text=和textPs=命令可访问这些方法。

`textPs=`提供了与使用Adobe Photoshop和Illustrator渲染的文本的高度相似性。 `text=`与使用Windows写字板呈现的文本相当兼容。

>[!NOTE]
>
>除了其他位置列出的差异之外，`text=`在渲染的文本中与`textPs=`相比还会产生细微的差异。 例如，下划线的厚度和位置不同，合成斜体以稍有不同的角度呈现。 如果文本不适合可用空间，`text=`可能会部分裁切最后一行，而`textPs=`只呈现完整的行。

所有文本命令都接受基于RTF（富文本格式）规范子集的格式化文本。 每个文本图层可以指定不同的文本命令。

下表列出了每个文本命令可用的主要功能：

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>功能</b> </th> 
   <th class="entry"> <b>文本=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b>另请参阅</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> 与Adobe Photoshop兼容 </p> </td> 
   <td> <p> 无 </p> </td> 
   <td> <p> 有限 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>将文本排成任意形状 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textFlowPath=， textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>沿任意路径排列文本 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>文本路径= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>复制管接头 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 复制管接头 <p>, <pre>\组排文字</pre>, <pre>\复制管线</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>文本框边距 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>完整的段落对齐 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最后一行对齐 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\lastql 、 \lastqr 、 \lastqc 、 \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落缩进 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\fi， \li， \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>全部大写字母和小型大写字母文本 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\caps， \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>图像服务颜色 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>多种消除锯齿模式 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>上下/右左文本流 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Photofont®支持 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 字体处理 </td> 
  </tr> 
  <tr> 
   <td> <p>自动调整图层大小以适合文本 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>text=， textId=， size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK支持 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\cmykcolortbl， \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>从右至左字符流 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>禁用自动换行 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>自动缩放文本以适合图层（通过改变分辨率） </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

可以手动装配RTF兼容字符串，也可以通过在能够保存RTF文件的文本编辑器或文字处理器中格式化所需的文本来装配RTF兼容字符串。 然后，可以使用纯文本编辑器打开RTF文件，并将文件的相关原始RTF内容复制到请求URL。

某些文字处理器会生成相当大的文件，其中包括动态媒体图像服务不使用的实质性前导码。 建议在将字符串传递到文本命令之前，从字符串中删除未使用的RTF元素。

RTF字符串支持基于UTF-8和ISO标准的语言编码，作为标准RTF字符编码机制的替代。 这允许应用程序在不了解RTF编码的情况下向服务器发送非英语文本。

如果要通过http传输字符串，则必须对所有非HTTP兼容字符进行正确转义。 如果字符串合并到图像目录记录的`catalog::Modifiers`字段中，则只需转义“=”、“&amp;”和“%”。 应始终删除控制字符，包括`<CR>`、`<LF>`和`<TAB>`。

图像服务文本引擎解释由富文本格式(RTF)规范版本1.6定义的命令子集。该子集侧重于字体/字符格式、简单的段落格式以及对国际字体和字符集的支持。 目前不支持更高级的格式结构，如样式表和表格。

尝试手动构建RTF编码的文本字符串时，需要熟悉由Microsoft发布的富文本格式(RTF)规范。

* [字体处理](r-font-handling.md)
* [颜色处理](r-color-handling.md)
* [复制管接头](r-copy-fitting.md)
* [文本图层](r-text-layers.md)
* [文本定位](r-text-positioning.md)
* [保留的字符](r-reserved-characters.md)
* [支持的RTF命令和关键字](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF编码示例](r-rtf-encoding-examples.md)
