---
description: 图像服务提供了多种渲染文本的替代方法，可通过text=和textPs=命令访问。
seo-description: 图像服务提供了多种渲染文本的替代方法，可通过text=和textPs=命令访问。
seo-title: 文本格式
solution: Experience Manager
title: 文本格式
topic: Scene7 Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Text formatting{#text-formatting}

图像服务提供了多种渲染文本的替代方法，可通过text=和textPs=命令访问。

`textPs=` 与使用Adobe Photoshop和Illustrator渲染的文本具有高度的相似性。 `text=` 与使用Windows写字板渲染的文本相当兼容。

>[!NOTE]
>
>除其他位置列出的差异外，与之相比， `text=` 渲染的文本也会产生细微的差异 `textPs=`。 例如，下划线的粗细和位置不相同，合成斜体以略微不同的角度呈现。 如果文本不适合可用空间，则可能会部分 `text=` 裁切最后一行，而只 `textPs=` 会渲染完整行。

所有文本命令都接受基于RTF（富文本格式）规范子集的格式化文本。 每个文本图层可指定不同的文本命令。

下表列表了每个文本命令可用的主要功能：

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 功能</b> </th> 
   <th class="entry"> <b> 文字=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> 另请参阅</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop兼容 </p> </td> 
   <td> <p> 无 </p> </td> 
   <td> <p> 有限 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>将文本排列为任意形状 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>沿任意路径排列文本 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>适合复制 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 复制适合 <p>, \copyfit, \copyfitlines, \copyfitmaxlines </p> </td> 
  </tr> 
  <tr> 
   <td> <p>文本框边距 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\margl, \margr, \margt, \margb </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落对齐 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\qj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最后一行对齐 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\lastql、\lastqr、\lastqc、\lastqc、\lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落缩进 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>全部大写和小写文本 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
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
   <td> <p>上下／左右文本排列 </p> </td> 
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
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK支持 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>从右至左的字符流 </p> </td> 
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

可以手动组合符合RTF规范的字符串，或者通过在能够保存RTF文件的文本编辑器或文字处理器中设置所需文本的格式来组合这些字符串。 然后，RTF文件可以在纯文本编辑器中打开，并且复制到请求URL的文件的相关原始RTF内容。

一些字处理器生成较大的文件，其中包括Scene7图像服务不使用的大量前导码。 建议先从字符串中删除未使用的RTF元素，然后再将字符串传递给文本命令。

RTF字符串中支持基于UTF-8和ISO标准的语言编码，作为标准RTF字符编码机制的替代方法。 这使应用程序无需了解RTF编码即可向服务器发送非英语文本。

如果要通过http传输字符串，则所有不符合HTTP的字符都必须正确转义。 如果字符串并入图像目录记录的字段，则只有&#39;=&#39;、&#39;&amp;&#39; `catalog::Modifiers` 和&#39;%&#39;需要转义。 应始终删除 `<CR>`包括、 `<LF>`和 `<TAB>` 在内的控制字符。

图像服务文本引擎解释由RTF(Rich Text Format)规范1.6版定义的一组命令。此子集侧重于字体／字符格式、简单的段落格式以及对国际字体和字符集的支持。 目前不支持更高级的格式构造，如样式表和表。

在尝试手动构建RTF编码的文本字符串时，需要熟悉Microsoft发布的RTF格式(RTF)规范。

* [字体处理](r-font-handling.md)
* [颜色处理](r-color-handling.md)
* [适合复制](r-copy-fitting.md)
* [文本图层](r-text-layers.md)
* [文本定位](r-text-positioning.md)
* [保留字符](r-reserved-characters.md)
* [支持的RTF命令和关键字](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF编码示例](r-rtf-encoding-examples.md)
