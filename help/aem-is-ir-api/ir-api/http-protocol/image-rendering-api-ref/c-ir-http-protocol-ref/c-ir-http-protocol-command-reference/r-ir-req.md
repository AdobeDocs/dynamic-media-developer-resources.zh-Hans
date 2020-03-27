---
description: 請求類型. 指定所请求的数据类型。
seo-description: 請求類型. 指定所请求的数据类型。
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dd13338-3457-477f-96e7-3ace7266d0ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# req{#req}

請求類型. 指定所请求的数据类型。

`req=debug|contents|img|imageprops|map|object|props|userdata|validate`

<table id="simpletable_D04D41FBB03D4992B257CCBAD7EF0E7B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 调试 </span> </p> </td> 
  <td class="stentry"> <p>在调试模式下运行命令。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 内容 </span> </p> </td> 
  <td class="stentry"> <p>返回有关暗角中对象的信息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> img </span> </p> </td> 
  <td class="stentry"> <p>运行命令并返回渲染后的图像。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> imageprops </span> </p> </td> 
  <td class="stentry"> <p>返回指定暗角的属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 地图 </span> </p> </td> 
  <td class="stentry"> <p>返回嵌入到暗角中的图像映射数据。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> object </span> </p> </td> 
  <td class="stentry"> <p>运行命令，并将渲染后的图像恢复为遮罩在当前对象选择中。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> prop </span> </p> </td> 
  <td class="stentry"> <p>运行命令并返回回复图像的属性。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 用户数据 </span> </p> </td> 
  <td class="stentry"> <p>返回晕影：: <span class="codeph"> UserData的内容 </span>。 </p> </td> 
 </tr> 
</table>

除非在详细说明中另有说明，否则服务器将返回MIME类型为&lt;text/plain>的文本响应。

`debug`

执行指定的命令并返回渲染后的图像。 如果发生错误，则返回错误和调试信息，而不是错误图像( `attribute::ErrorImagePath`)。

`contents`

返回晕影中对象层次的XML表示形式，包括所选对象属性。 请求中的其他命令将被忽略。

`img`

执行指定的命令并返回渲染后的图像。 回复数据格式和响应类型由确定 `fmt=`。

`imageprops`

返回在URL路径中指定的晕影文件或目录条目的选定属性。 有关 [回复语法](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 和响应MIME类型的说明，请参阅属性。 请求中的其他命令将被忽略。 返回以下属性：

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
   <td colname="col3"> <p> <span class="codeph"> 属性：：到期 </span> 或默认的有效时间。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>全分辨率高度（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>与此晕影关联的用户档案的名称／说明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embeddedIccProfile </span> </p> </td> 
   <td colname="col2"> <p>布尔值 </p> </td> 
   <td colname="col3"> <p>1.如果关联用户档案嵌入到暗角中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.embedded PhotoshopPaths </span> </p> </td> 
   <td colname="col2"> <p>布尔值 </p> </td> 
   <td colname="col3"> <p>1.如果暗角嵌入了路径数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.modifier </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 属性：：修改 </span> 量，如果不是目录条目则为空。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td colname="col2"> <p>Enum </p> </td> 
   <td colname="col3"> <p>响应图像的像素类型；可以是“CMYK”、“RGB”或“BW”（对于灰度图像）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>默认打印分辨率(dpi)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.timeStamp </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>修改日期／时间(来 <span class="codeph"> 自目录：:TimeStamp </span> 或暗角文件)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>全分辨率宽度（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.name </span> </p> </td> 
   <td colname="col2"> <p>字符串型 </p> </td> 
   <td colname="col3"> <p>暗角名称（根暗角对象的名称字符串）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>最大对象分辨率， <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 以材料分 </a> 辨率单位（通常为像素／英寸）表示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 暗角。res.avg </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>以材料分辨率 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 单位(通 </a> 常为像素/inc材料分辨率 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"></a>h)表示的平均对象分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.res.min </span> </p> </td> 
   <td colname="col2"> <p>Real </p> </td> 
   <td colname="col3"> <p>最小对象分辨率 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b" type="concept" format="dita" scope="local"> 以材料分 </a> 辨率单位（通常为像素／英寸）表示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vignette.version </span> </p> </td> 
   <td colname="col2"> <p>整型 </p> </td> 
   <td colname="col3"> <p>晕影文件版本号。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`map`

返回包含在暗角中的图像映射数据。 默认情况下，返回所有最外面的组的映射数据。 可以使用

`req=map&groupLevel=-1`

映射数据不会缩放到或以其 `wid=` 他方 `hei=` 式修改。 响应MIME类型为 `<text/xml>`。

响应数据由包含一组 `<map>` 元素的元素组成， `<area>` 与HTML标签类似 `<AREA>` 。

每个 `<area>` 元素都包括标准和属 `type=` 性 `coord=``name=` 以及一个属性，用于指定晕影组名称或名称路径。 如果 `<area>` 相应对象组的蒙版具有不连续的区域，则存在多个同名的元素。

除了默认属性外，晕影还可以定义其他属性（如果创作了这些属性）。 此类自定义属性定义为对象组属性。 自定义属性的名称必须以开头 `map`。 要包含在元素 `<area>` 中。 例如，如果组属性包括 `map.href=http://www.scene7.com`，则相应的元 `<area>` 素将包括 `href="http://www.scene7.com"`。

如果暗角不包括映射数 `<map>` 据，则返回一个包含空元素的XML文档。

`object`

执行指定的命令并返回由剩余对象选择（请求中使用最后一个或命令选择的组或对象）遮 `sel=` 罩的 `obj=` 渲染的图像。 通常与支持alpha的图像格式一起使用(请参 [阅fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c))。 如果使用不支持alpha的图像格式，则遮罩外的区域为黑色。

`props`

执行指定的命令并返回晕影属性和组或对象属性，而不是渲染的图像。 有关 [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a) 回复语法和响应MIME类型的说明，请参阅属性。 除非也指定或 `obj=` 指定 `sel=` ，否则将应用默认选择(请参 [ 阅 `obj=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a))。

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
   <td> <p> 返回图像高度（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p>如果ICC用户档案将嵌入到回复图像中，则为true(请参阅 <span class="codeph"> iccEmbed= <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f" type="reference" format="dita" scope="local"></a></span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 与回复图像关联的用户档案的快捷键名称(请参 <span class="codeph"> 阅 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06" type="reference" format="dita" scope="local"> icc= </a></span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p> 如果回复图像包含alpha，则为true。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> 布尔值 </p> </td> 
   <td> <p> 如果回复图像包含路径数据，则返回为true(请参 <span class="codeph"> 阅 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f" type="reference" format="dita" scope="local"> pathEmbed= </a></span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 回复图像类型，可为“CMYK”、“RGB”或“BW”（对于灰度图像） </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> Real </p> </td> 
   <td> <p> 打印分辨率(dpi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p>整数，布尔值 </p> </td> 
   <td> <p> JPEG质量和色度标志(请参 <span class="codeph"> 阅 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd" type="reference" format="dita" scope="local"> qlt= </a></span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 回复图像的MIME类型(请参 <span class="codeph"> 阅 <a href="../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c" type="reference" format="dita" scope="local"> fmt= </a></span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 返回图像宽度（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.attributes </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 当前选择的属性字符串。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.count </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选择中的对象数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.ident </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 缩进当前选定内容的值。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 选择 <span class="codeph"> selection.attributes </span>ion.name </span> </p> </td> 
   <td> <p> 字符串型 </p> </td> 
   <td> <p> 当前所选对象的完整名称路径。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.overlapping </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选择中重叠对象的数量。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.renderable </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p>当前选择中可渲染的对象数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.texturable </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选择中可纹理化对象的数量。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.visible </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选择的显示／隐藏状态。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> selection.zorder </span> </p> </td> 
   <td> <p> 整型 </p> </td> 
   <td> <p> 当前选择中第一个重叠对象的Z顺序值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`userdata`

返回的内容 `vignette::UserData`。 服务器将用行终结器() `'??'` 替换 `vignette::UserData` 所有出现的 `<cr><lf>`事件。 回复的格式设置为文本数据，响应MIME类型设置为&lt;text/plain>。

如果URL路径中指定的对象未解析为有效的晕影映射条目，或者如果该对象为空，则回复将仅包含行终止符( `vignette::UserData``CR/LF`)。

将忽略请求字符串中的任何其他命令。

## 属性 {#section-e44092e190ff4f6380583e8ed6ea5b0b}

请求命令。 可能出现在请求字符串中的任意位置。

## 默认 {#section-00c593cbf1af4364b6b78812e6b93c64}

如果URL不包括图像路径或修饰符，则：

```
#S7Z OK 
#Mon Aug 18 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Otherwise, `req=img`

## 另请参阅 {#section-f7a955525fb44ef2ae7cd7ede25a96c3}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c) ，属 [性：:ErrorImagePath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)，暗角 [::UserData](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85)，属 [性](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-response-data/c-ir-properties.md#concept-e99f1a373eae4af9b41842ca0088ad3a)
