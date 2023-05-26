---
description: 图像服务提供了一种机制，用于获取表示与特定记录的目录ImageSet关联的所有资源和元数据的分层文本响应（xml或json）。
solution: Experience Manager
title: 媒体集请求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 0%

---

# 媒体集请求{#media-set-requests}

图像服务提供了一种机制，用于获取表示与特定记录的catalog：：ImageSet关联的所有资源和元数据的分层文本响应（xml或json）。

观看者可以使用此机制生成响应，以告知简单图像、视频、视频集、样本集、旋转集、页面集(e-catalog)和媒体集的呈现。

## 请求语法 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

设置的响应 `catalog::ImageSet` 可以通过以下方式检索： `req=set` 修饰符和引用net路径中的目录记录id。 或者，可以使用直接在URL中指定图像集 `imageset=` 修饰符。 如果 `imageset=` 修饰符用于指定图像集，整个值应括在大括号中，以便转义图像集值并确保包含的任何修饰符不会解释为URL查询字符串的一部分。

## 设置的响应类型 {#section-93eb0a1f70344da2a888e56372ad3896}

设置机制支持以下类型的响应：

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>简单图像 </p></td> 
  <td class="stentry"> <p>图像记录，但不包含 <span class="codeph"> catalog：：图像集</span> 已定义。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>简单视频 </p></td> 
  <td class="stentry"> <p>静态内容目录中的视频记录。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>样本集 </p></td> 
  <td class="stentry"> <p>一组项，包含对图像记录的引用和对用作色板的图像记录的可选单独引用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>分层样本集 </p></td> 
  <td class="stentry"> <p>由基本样本项或样本集记录引用组成的一组项。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>旋转集 </p></td> 
  <td class="stentry"> <p>由图像ID的简单列表组成的一组项目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>二维旋转集 </p></td> 
  <td class="stentry"> <p>由简单图像或基本旋转集的引用组成的一组项目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>页面集 </p></td> 
  <td class="stentry"> <p>一组项目，由最多三个页面图像的列表组成 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒体集 </p></td> 
  <td class="stentry"> <p>一组项目，由简单图像、视频集、样本集、分层样本集、旋转集、二维旋转集、页面集和视频资产组成。 每个媒体集项目也可以包含一个可选色板。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>视频集 </p></td> 
  <td class="stentry"> <p>由简单视频列表组成的一组项目。 </p></td> 
 </tr> 
</table>

## 外部集类型检测 {#section-3dd6e453528d46898e559d31458a59ba}

当 `req=set` 收到请求后，要生成的响应类型由的值确定 `catalog::AssetType`. 如果 `catalog::AssetType` 未定义，则响应类型由以下规则确定：

* 如果在图像目录中找到记录，并且 `catalog::ImageSet` 已定义

   * 如果记录图像集字段中至少有一个条目包含冒号，则假定已设置e目录
   * 如果记录图像集字段中至少有一个条目包含两个分号，则假定媒体集。
   * 如果记录图像集字段中至少有一个条目包含一个分号，则假定图像集。
   * 如果没有任何条目包含冒号或分号，但至少有一个条目包含引用的集或内联集（这是2D旋转集），则假定为旋转集。
   * 如果没有条目包含冒号、分号、引用的集或内嵌集（即逗号分隔的图像列表），则假定为未知集。

* 如果在图像和静态内容目录中都找到了记录

   * 如果文件扩展名在以下集中，则假定为视频： mp3、mp4、flv、f4v、swf、xml
   * 否则，假定图像

* 如果在静态内容目录中找到记录，但在图像目录中找不到记录

   * 如果文件扩展名在以下集中，则假定为视频： mp3、mp4、flv、f4v、swf、xml
   * 假设为静态，否则

* 如果在图像目录中找到记录，但在静态内容目录中找不到记录，则

   * 假设图像

* 如果在图像目录中未找到记录，则在静态内容目录中未找到记录

   * 如果文件扩展名在以下集中，则假定是基于文件的视频： mp3、mp4、flv、f4v、swf、xml
   * 否则，假定使用基于文件的图像

在所有情况下，生成的xml响应都将符合指定的XML文档，并且设置的根节点对应于检测到的类型。

## 内集类型检测 {#section-8f46490e467247e69ce284704def06f3}

当检测到外部集为类型媒体集时，响应将包含一组媒体集项目，这些项目与中的每个媒体集项目相对应。 `catalog::ImageSet`. 如果为特定媒体集条目指定了可选的类型参数，则会根据下表将其映射到输出类型：

| 输入类型 | 输出类型 |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

如果没有为特定媒体集条目指定可选的类型参数，或者该参数对应于不受支持的类型，则使用与在外层媒体集级别应用的规则相同的规则自动检测媒体集项目类型。

## XML规范 {#section-c1bd60948ef545759a16885bb6fcc607}

返回的xml响应符合以下规范：

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## 标签键 {#section-bf565de6f7294cf89620343c9071f415}

此 `labelkey=` 修饰符与 `catalog::UserData`用于为图像和样本生成标签的字段。 此 `catalog:UserData` 字段解析为一组键/值对，并且其中的标签键索引用于检索给定键的值。 此值随后返回到 *`l`* 属性 *`s`* 和 *`i`*.

## 强制限制 {#section-b9f042873bee45a5ae11b69fd42f2bca}

为了限制响应大小并防止自引用问题，最大嵌套深度由服务器属性控制 `PS::fvctx.nestingLimit`. 如果超过此限制，则会返回错误。

为了限制大型e-catalog集的xml响应的大小，根据服务器属性禁止小册子集项目的私有元数据 `PS::fvctx.brochureLimit`. 与宣传册关联的所有专用元数据都将导出，直到达到宣传册限制为止。 超过限制后，将禁止专用映射和用户数据，并设置相应标志以指示禁止的数据类型。

不支持嵌套媒体集。 嵌套媒体集定义为包含媒体集类型的媒体集项目的媒体集。 如果检测到此情况，则会返回错误。

## 示例 {#section-588c9d33aa05482c86cd2b1936887228}

对于示例XML响应 `req=set` 请求，请参阅HTML示例标题下的“属性”页面。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 另请参阅 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ， [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3)， [catalog：：图像集](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)， [图像目录引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
