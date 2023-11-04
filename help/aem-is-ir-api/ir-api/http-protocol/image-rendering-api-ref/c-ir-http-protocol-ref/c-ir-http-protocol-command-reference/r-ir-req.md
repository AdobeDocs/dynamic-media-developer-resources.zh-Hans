---
title: 需要
description: 請求類型. 指定请求的数据类型。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b4a78a1-4f03-47ce-b523-10975e83f0ea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '947'
ht-degree: 4%

---

# 需要{#req}

請求類型. 指定请求的数据类型。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 调试 </span> </p> </td> 
  <td class="stentry"> <p>在调试模式下运行命令。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 内容 </span> </p> </td> 
  <td class="stentry"> <p>返回有关晕影中对象的信息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>运行命令并返回渲染的图像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>返回指定晕影的属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 地图 </span> </p> </td> 
  <td class="stentry"> <p>返回晕影中嵌入的图像映射数据。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object </span> </p> </td> 
  <td class="stentry"> <p>运行命令并将蒙版的渲染图像返回到当前对象选择。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> prop </span> </p> </td> 
  <td class="stentry"> <p>运行命令并返回回复图像的属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 用户数据 </span> </p> </td> 
  <td class="stentry"> <p>返回以下内容 <span class="codeph"> 晕影：：UserData </span>. </p> </td> 
 </tr> 
</table>

除非在详细描述中另有说明，否则服务器将返回MIME类型的文本响应 &lt;text plain=&quot;&quot;>.

`debug`

执行指定的命令并返回渲染的图像。 如果发生错误，将返回错误和调试信息而不是错误图像( `attribute::ErrorImagePath`)。

`contents`

返回晕影中对象层次结构的XML表示形式，包括所选对象属性。 请求中的其他命令将被忽略。

`img`

执行指定的命令并返回渲染的图像。 回复数据格式和响应类型由 `fmt=`.

`imageprops`

返回在URL路径中指定的晕影文件或目录条目的所选属性。 请参阅 [属性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 有关回复语法和响应MIME类型的说明。 请求中的其他命令将被忽略。 将返回以下属性：

<table id="table_A30296D29B5D43F1B5383A887252C6B4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.expiration </span> </p> </td> 
   <td colname="col2"> <p>多次 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute：：Expiration </span> 或默认生存时间。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>以像素为单位的完整分辨率高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>与此晕影关联的配置文件的名称/描述。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>布尔值 </p> </td> 
   <td colname="col3"> <p>1（如果关联的配置文件嵌入在晕影中）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>布尔值 </p> </td> 
   <td colname="col3"> <p>1（如果晕影嵌入了路径数据）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute：：Modifier </span> 如果没有目录条目，则为空。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>枚举 </p> </td> 
   <td colname="col3"> <p>响应图像的像素类型；可以是“CMYK”、“RGB”或“BW”（适用于灰度图像）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>实数 </p> </td> 
   <td colname="col3"> <p>默认打印分辨率（以dpi为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>修改日期/时间(从 <span class="codeph"> catalog：：时间戳 </span> 或晕影文件)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>以像素为单位的完整分辨率宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>晕影名称（根晕影对象的名称字符串）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 晕影.res </span> </p> </td> 
   <td colname="col2"> <p>实数 </p> </td> 
   <td colname="col3"> <p>中的最大对象分辨率 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材质分辨率 </a> 单位（通常为像素/英寸）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.avg </span> </p> </td> 
   <td colname="col2"> <p>实数 </p> </td> 
   <td colname="col3"> <p>中的平均对象分辨率 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材质分辨率 </a> 单位（通常为像素/inc） <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材质分辨率 </a>h)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 晕影.res.min </span> </p> </td> 
   <td colname="col2"> <p>实数 </p> </td> 
   <td colname="col3"> <p>中的最小对象分辨率 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 材质分辨率 </a> 单位（通常为像素/英寸）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>晕影文件版本号。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

返回晕影中包含的图像映射数据。 默认情况下，将返回所有最外部组的映射数据。 可以使用获取所有最内层的组的映射数据

`req=map&groupLevel=-1`

映射数据不会缩放到 `wid=` 或 `hei=` 或进行其他修改。 响应MIME类型为 `<text/xml>`.

响应数据包含 `<map>` 元素包含一组 `<area>` 元素，类似于HTML `<AREA>` 标记之前。

每个 `<area>` 元素包括标准 `type=` 和 `coord=` 属性，和 `name=` 属性，指定晕影组名称或名称路径。 多个 `<area>` 如果相应对象组的掩码具有不连续的区域，则存在同名元素。

除了默认属性之外，如果已经创作，晕影还可以定义其他属性。 此类自定义属性被定义为对象组属性。 自定义属性的名称必须以开头 `map` 将包含在 `<area>` 元素。 例如，如果组属性包括 `map.href=http://www.scene7.com`，相应的 `<area>` 元素包括 `href="http://www.scene7.com"`.

带空的XML文档 `<map>` 如果晕影不包含映射数据，则返回元素。

`object`

执行指定的命令并返回由剩余对象选择（用最后一个对象选择的组或对象）遮罩的渲染图像 `sel=` 或 `obj=` 命令)。 通常与支持Alpha的图像格式一起使用(请参阅 [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c))。 如果使用的图像格式不支持alpha，则蒙版外部的区域为黑色。

`props`

执行指定的命令并返回晕影属性和组或对象属性，而不是渲染的图像。 请参阅 [属性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 有关回复语法和响应MIME类型的说明。 除非出现以下情况，否则将应用默认选择 `obj=` 或 `sel=` 也指定(请参阅 [`obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a))。

响应中可能包含以下属性：

<table id="table_F3ECF0584F6247A2A75C1CAFE1C57A4E"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p> 类型 </p> </th> 
   <th class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 回复图像背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p>整型 </p> </td> 
   <td> <p> 回复图像高度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p>如果ICC配置文件嵌入到回复图像中，则为True(请参阅 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"> iccEmbed= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 与回复图像关联的配置文件的快捷方式名称(请参阅 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p> 如果回复图像包含Alpha，则为True。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p> 如果回复图像包含路径数据，则为True(请参阅 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 回复图像类型，可以是“CMYK”、“RGB”或“BW”（用于灰度图像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> 实数 </p> </td> 
   <td> <p> 打印分辨率(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>整数，布尔值 </p> </td> 
   <td> <p> JPEG质量和色度标志(请参阅 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a> </span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 回复图像的MIME类型(请参阅 <span class="codeph"> <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a> </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 回复图像宽度（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 选择属性 </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 当前选择的属性字符串。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 选择计数 </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选定内容中的对象数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选定内容的缩进值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 选择 <span class="codeph"> 选择属性 </span>ion.name </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 当前对象选择的全名路径。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overling </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选定内容中的重叠对象数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p>当前选区中可呈现对象的数量。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选定内容中的可纹理对象数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前显示/隐藏当前选择的状态。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选择中第一个重叠对象的Z顺序值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

返回以下内容 `vignette::UserData`. 服务器将替换所有出现的 `'??'` 在 `vignette::UserData` 带有行终止符( `<cr><lf>`)。 将回复格式化为响应MIME类型设置为的文本数据 &lt;text plain=&quot;&quot;>.

如果URL路径中指定的对象未解析为有效的晕影映射条目，或者 `vignette::UserData` 为空，则回复仅包含行结束符( `CR/LF`)。

请求字符串中的任何其他命令都将被忽略。

## 属性 {#section-e44092e190ff4f6380583e8ed6ea5b0b}

请求命令。 可能出现在请求字符串中的任何位置。

## 默认 {#section-00c593cbf1af4364b6b78812e6b93c64}

如果URL不包含图像路径或修改符，则：

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

否则， `req=img`

## 另请参阅 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ， [属性：：ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)， [晕影：：UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85)， [属性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
