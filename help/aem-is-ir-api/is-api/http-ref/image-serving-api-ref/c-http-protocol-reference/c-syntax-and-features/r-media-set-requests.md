---
description: 图像服务提供了一种用于获取分层文本响应（xml或json）的机制，该文本响应表示与特定记录的目录ImageSet关联的所有资源和元数据。
solution: Experience Manager
title: 媒体集请求
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# 媒体集请求{#media-set-requests}

图像服务提供了一种用于获取分层文本响应（xml或json）的机制，该响应表示与特定记录的catalog：：ImageSet关联的所有资源和元数据。

观看者可以使用此机制生成响应，以通知简单图像、视频、视频集、样本集、旋转集、页面集(e-catalog)和媒体集的呈现。

## 请求语法 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

可以使用`catalog::ImageSet`修饰符并引用Net路径中的目录记录ID来检索`req=set`的设置响应。 或者，可以使用`imageset=`修饰符直接在URL中指定图像集。 如果使用`imageset=`修饰符指定图像集，则应将整个值括在大括号中，以便对图像集值进行转义，并确保所包含的任何修饰符均不会解释为URL查询字符串的一部分。

## 集合响应的类型 {#section-93eb0a1f70344da2a888e56372ad3896}

设置机制支持以下类型的响应：

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>简单图像 </p></td> 
  <td class="stentry"> <p>定义了没有<span class="codeph">目录：：ImageSet</span>的图像记录。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>简单视频 </p></td> 
  <td class="stentry"> <p>静态内容目录中的视频记录。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>样本集 </p></td> 
  <td class="stentry"> <p>一组项目，包括对图像记录的引用和对用作色板的图像记录的可选单独引用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>分层样本集 </p></td> 
  <td class="stentry"> <p>由基本样本项或样本集记录的引用组成的一组项。 </p></td> 
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
  <td class="stentry"> <p>一组项目，由最多包含三个页面图像的列表组成 </p></td> 
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

## 外集类型检测 {#section-3dd6e453528d46898e559d31458a59ba}

收到`req=set`请求时，要生成的响应类型由`catalog::AssetType`的值决定。 如果未定义`catalog::AssetType`，则响应类型由以下规则确定：

* 如果在图像目录中找到记录并且定义了`catalog::ImageSet`

   * 如果记录图像集字段中至少有一个条目包含冒号，则假定已设置e目录
   * 如果记录“图像集”字段中至少有一个条目包含两个分号，则假定媒体集。
   * 如果记录图像集字段中至少有一个条目包含一个分号，则假定图像集。
   * 如果没有任何条目包含冒号或分号，但至少有一个条目包含引用集或内联集（这是2D旋转集），则假定为旋转集。
   * 如果没有条目包含冒号、分号、引用的集或内嵌集（即以逗号分隔的图像列表），则假定为未知集。

* 如果在图像和静态内容目录中都找到了记录

   * 如果文件扩展名在以下集中，则假定为视频： mp3、mp4、flv、f4v、swf、xml
   * 否则，假设图像

* 如果在静态内容目录中找到记录，但在图像目录中找不到记录

   * 如果文件扩展名在以下集中，则假定为视频： mp3、mp4、flv、f4v、swf、xml
   * 假设为静态，否则

* 如果在图像目录中找到记录，但在静态内容目录中未找到记录，则为

   * 假设图像

* 如果在图像目录中未找到记录，在静态内容目录中未找到记录

   * 如果文件扩展名在以下集中，则假定使用基于文件的视频： mp3、mp4、flv、f4v、swf、xml
   * 否则，采用基于文件的图像

在所有情况下，生成的xml响应都符合指定的XML文档，并且设置的根节点与检测到的类型相对应。

## 内集型检测 {#section-8f46490e467247e69ce284704def06f3}

当检测到外部集为类型媒体集时，响应包含一组与`catalog::ImageSet`中的每个媒体集条目对应的媒体集项目。 如果为特定媒体集条目指定了可选的类型参数，则会根据下表将其映射到输出类型：

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

如果未指定特定媒体集项的可选类型参数，或者该参数对应于不支持的类型，则使用与在外层媒体集级别应用的规则相同的规则自动检测媒体集项类型。

## XML规范 {#section-c1bd60948ef545759a16885bb6fcc607}

返回的xml响应符合以下规范：

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## 标签键 {#section-bf565de6f7294cf89620343c9071f415}

`labelkey=`修饰符与`catalog::UserData`字段一起使用，以生成图像和样本的标签。 `catalog:UserData`字段被解析为一组键/值对，该组中的标签键索引用于检索给定键的值。 此值随后在&#x200B;*`l`*&#x200B;和&#x200B;*`s`*&#x200B;的&#x200B;*`i`*&#x200B;特性中返回。

## 强制限制 {#section-b9f042873bee45a5ae11b69fd42f2bca}

为了限制响应大小并防止出现自引用问题，最大嵌套深度由服务器属性`PS::fvctx.nestingLimit`控制。 如果超过此限制，则会返回错误。

为了限制大型e-catalog集的xml响应大小，根据服务器属性`PS::fvctx.brochureLimit`，禁止小册子集项目的私有元数据。 与宣传册关联的所有私有元数据都将导出，直到达到宣传册限制为止。 超过限制后，将禁止专用映射和用户数据，并设置相应标志以指示禁止的数据类型。

不支持嵌套媒体集。 嵌套媒体集被定义为包含媒体集类型的媒体集项目的媒体集。 如果检测到此情况，则会返回错误。

## 示例 {#section-588c9d33aa05482c86cd2b1936887228}

有关`req=set`请求的示例XML响应，请参阅HTML示例标题下的属性页面。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 另请参阅 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ，[图像集=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3)，[目录：：图像集](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)，[图像目录引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
