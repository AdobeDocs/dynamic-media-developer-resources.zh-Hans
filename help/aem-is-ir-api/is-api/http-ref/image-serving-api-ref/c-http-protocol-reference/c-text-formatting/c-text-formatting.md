---
description: 图像服务提供了多种渲染文本的替代方法，可通过text=和textPs=命令访问。
seo-description: 图像服务提供了多种渲染文本的替代方法，可通过text=和textPs=命令访问。
seo-title: 文本格式
solution: Experience Manager
title: 文本格式
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 6%

---


# 文本格式{#text-formatting}

图像服务提供了多种渲染文本的替代方法，可通过text=和textPs=命令访问。

`textPs=` 提供与使用Adobe Photoshop和Illustrator渲染的文本高度相似的内容。`text=` 与使用Windows写字板渲染的文本相当兼容。

>[!NOTE]
>
>除其他位置列出的差异外，与`textPs=`相比，`text=`在呈现的文本中会产生细微的差异。 例如，下划线的厚度和位置不相同，合成斜体以略微不同的角度进行渲染。 如果文本不适合可用空间，`text=`可能会部分裁剪最后一行，而`textPs=`将仅渲染完整行。

所有文本命令都接受基于RTF（富文本格式）规范子集的格式化文本。 每个文本图层可以指定不同的文本命令。

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
   <td> <p>复制适合 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> 复制适合 <p>, <pre>\文本适应</pre>, <pre>\组排行</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>文本框边距 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\marg</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落对齐 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最后一行对齐 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\lastql、\lastqr、\lastqc、\lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落缩进 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\fi、\li、\ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>所有大写和小写文本 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\caps，\scaps </p> </td> 
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
   <td> <p>上下/左右文本排列 </p> </td> 
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
   <td> <p>text=,textId=,size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK支持 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>\cmykcolortbl， \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>从右到左的字符流 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>禁用换行 </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>自动缩放文本以适合图层（通过不同分辨率） </p> </td> 
   <td> <p>是 </p> </td> 
   <td> <p>无 </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

可手动组合符合RTF的字符串，或通过在能够保存RTF文件的文本编辑器或文字处理器中设置所需文本的格式来组合字符串。 然后，RTF文件可以在纯文本编辑器中打开，并且文件的相关原始RTF内容被复制到请求URL。

某些字处理器生成较大的文件，其中包括Dynamic Media图像服务不使用的大量前导。 建议先从字符串中删除未使用的RTF元素，然后再将字符串传递给文本命令。

RTF字符串支持基于UTF-8和ISO标准的语言编码，作为标准RTF字符编码机制的替代方法。 这样，应用程序就可以在不了解RTF编码的情况下向服务器发送非英语文本。

如果要通过http传输字符串，则必须正确转义所有不符合HTTP的字符。 如果字符串并入到图像目录记录的`catalog::Modifiers`字段，则只有“=”、“&amp;”和“%”需要转义。 应始终删除控制字符，包括`<CR>`、`<LF>`和`<TAB>`。

“图像服务”文本引擎解释由RTF格式(RTF)规范1.6版定义的命令子集。此子集侧重于字体/字符格式、简单段落格式以及支持国际字体和字符集。 目前不支持更高级的格式构造，如样式表和表。

在尝试手动构建RTF编码的文本字符串时，需要熟悉Microsoft发布的RTF格式(RTF)规范。

* [字体处理](r-font-handling.md)
* [颜色处理](r-color-handling.md)
* [复制适合](r-copy-fitting.md)
* [文本图层](r-text-layers.md)
* [文本定位](r-text-positioning.md)
* [保留字符](r-reserved-characters.md)
* [支持的RTF命令和关键字](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF编码示例](r-rtf-encoding-examples.md)
