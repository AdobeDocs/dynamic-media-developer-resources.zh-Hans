---
description: 图像服务提供了一种获取层级文本响应（xml或json）的机制，该响应表示与特定记录的目录ImageSet关联的所有资源和元数据。
solution: Experience Manager
title: 媒体集请求
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 0%

---

# 媒体集请求{#media-set-requests}

图像提供提供了一种获取层级文本响应（xml或json）的机制，该响应表示与目录：:ImageSet（特定记录）关联的所有资源和元数据。

查看器可以使用此机制生成响应，以通知演示简单图像、视频、视频集、色板集、旋转集、页面集（电子目录）和媒体集。

## 请求语法 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

可以使用`req=set`修饰符并引用净路径中的目录记录ID来检索`catalog::ImageSet`的集响应。 或者，也可以使用`imageset=`修饰符直接在URL中指定图像集。 如果使用`imageset=`修饰符指定图像集，则应将整个值括在大括号中，以转义图像集值，并确保任何包含的修饰符都未解释为URL查询字符串的一部分。

## 集响应的类型 {#section-93eb0a1f70344da2a888e56372ad3896}

设置机制支持以下类型的响应：

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>简单图像 </p></td> 
  <td class="stentry"> <p>未定义<span class="codeph">目录的图像记录：:ImageSet</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>简单视频 </p></td> 
  <td class="stentry"> <p>静态内容目录中的视频记录。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>色板集 </p></td> 
  <td class="stentry"> <p>一组项目，包括对图像记录的引用和对用作样本的图像记录的可选单独引用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>分层样本集 </p></td> 
  <td class="stentry"> <p>由基本色板项目或对色板集记录的引用组成的项目集。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>旋转集 </p></td> 
  <td class="stentry"> <p>一组由简单的图像ID列表组成的项目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>二维旋转集 </p></td> 
  <td class="stentry"> <p>由简单图像或对基本旋转集的引用组成的项目集。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>页面集 </p></td> 
  <td class="stentry"> <p>一组项目，包含最多三个页面图像的列表 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒体集 </p></td> 
  <td class="stentry"> <p>一组项目，由简单图像、视频集、样本集、分层样本集、旋转集、二维旋转集、页面集和视频资产组成。 每个媒体集项目还可以包含一个可选色板。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>视频集 </p></td> 
  <td class="stentry"> <p>一组由简单视频列表组成的项目。 </p></td> 
 </tr> 
</table>

## 外置式检测 {#section-3dd6e453528d46898e559d31458a59ba}

当收到`req=set`请求时，要生成的响应类型由`catalog::AssetType`的值确定。 如果未定义`catalog::AssetType`，则响应类型由以下规则确定：

* 如果在图像目录中找到记录，并且定义了`catalog::ImageSet`

   * 如果记录“图像集”字段中至少有一个条目包含冒号，则假定已设置电子目录
   * 如果“记录图像集”字段中至少有一个条目包含两个分号，则假定已设置媒体。
   * 如果记录“图像集”字段中至少有一个条目包含一个分号，则假定已设置图像。
   * 如果没有条目包含冒号或分号，但至少有一个条目包含引用集或内嵌集（这是2D旋转集），则假设旋转集。
   * 如果没有条目包含冒号、分号、引用集或行内集（即以逗号分隔的图像列表），则假设未知集。

* 如果在图像和静态内容目录中都找到记录

   * 如果文件扩展名位于以下设置中，则假定为视频：mp3、mp4、flv、f4v、swf、xml
   * 假设图像

* 如果在静态内容目录中找到记录，但未在图像目录中找到记录

   * 如果文件扩展名位于以下设置中，则假定为视频：mp3、mp4、flv、f4v、swf、xml
   * 假设为静态，否则为静态

* 如果记录在图像目录中找到，但未在静态内容目录中找到

   * 假定图像

* 如果记录在图像目录中未找到，且在静态内容目录中未找到

   * 如果文件扩展名位于以下设置中，则假定基于文件的视频：mp3、mp4、flv、f4v、swf、xml
   * 假定基于文件的图像，否则

在所有情况下，生成的xml响应都将符合指定的XML文档，并且其设置的根节点对应于检测到的类型。

## 内置式检测 {#section-8f46490e467247e69ce284704def06f3}

当检测到外部集为类型媒体集时，响应将包含与`catalog::ImageSet`中的每个媒体集条目对应的媒体集项目集。 如果为特定媒体集条目指定了可选类型参数，则会根据下表将其映射到输出类型：

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

如果未指定特定媒体集条目的可选类型参数或与不支持的类型对应，则使用与在外部集级别应用的相同规则自动检测媒体集项目类型。

## XML规范 {#section-c1bd60948ef545759a16885bb6fcc607}

返回的xml响应符合以下规范：

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

`labelkey=`修饰符与`catalog::UserData`字段一起使用，为图像和色板生成标签。 `catalog:UserData`字段将解析为一组键/值对，并且中的标签键索引将在此集中检索给定键的值。 然后，该值会在&#x200B;*`s`*&#x200B;和&#x200B;*`i`*&#x200B;的&#x200B;*`l`*&#x200B;属性中返回。

## 强制限制 {#section-b9f042873bee45a5ae11b69fd42f2bca}

为了限制响应的大小并防止自引用问题，最大嵌套深度由服务器属性`PS::fvctx.nestingLimit`控制。 如果超出此限制，则返回错误。

为了限制大型电子目录集的xml响应的大小，根据服务器属性`PS::fvctx.brochureLimit`禁止手册集项的专用元数据。 与手册关联的所有专用元数据都将导出，直到达到手册限制为止。 一旦超出限制，将禁止专用映射和用户数据，并设置相应的标志以指示禁止哪种类型的数据。

不支持嵌套媒体集。 嵌套媒体集定义为包含媒体集类型的媒体集项目的媒体集。 如果检测到此情况，将返回错误。

## 示例 {#section-588c9d33aa05482c86cd2b1936887228}

有关`req=set`请求的XML响应示例，请参阅HTML示例标题下的属性页。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 另请参阅 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3),  [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md),  [Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
