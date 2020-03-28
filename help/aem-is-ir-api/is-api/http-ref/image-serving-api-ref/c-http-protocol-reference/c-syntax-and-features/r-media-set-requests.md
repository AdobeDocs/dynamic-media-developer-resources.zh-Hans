---
description: 图像服务提供了一种获取层次文本响应（xml或json）的机制，该响应表示与特定记录的目录ImageSet关联的所有资源和元数据。
seo-description: 图像服务提供了一种获取层次文本响应（xml或json）的机制，该响应表示与特定记录的目录ImageSet关联的所有资源和元数据。
seo-title: 媒体集请求
solution: Experience Manager
title: 媒体集请求
topic: Scene7 Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 媒体集请求{#media-set-requests}

图像服务提供了获取层次文本响应（xml或json）的机制，该响应表示与catalog:::ImageSet关联的所有资源和元数据，用于特定记录。

查看器可以使用此机制生成响应，以通知演示简单图像、视频、视频集、样本集、旋转集、页面集(e-catalogs)和媒体集。

## 请求语法 {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

可以使用修饰符并引 `catalog::ImageSet` 用净路径中的目录记录id, `req=set` 检索对某个的集响应。 或者，也可以使用修饰符直接在URL中指定图像 `imageset=` 集。 如果使 `imageset=` 用修饰符指定图像集，则整个值应用大括号括起来，以转义图像集值，并确保包含的修饰符不被解释为URL查询字符串的一部分。

## 集合响应的类型 {#section-93eb0a1f70344da2a888e56372ad3896}

设置机制支持以下类型的响应：

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>简单的图像 </p></td> 
  <td class="stentry"> <p>未定义目录 <span class="codeph"> 的图像记录：:ImageSet</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>简单的视频 </p></td> 
  <td class="stentry"> <p>静态内容目录中的视频记录。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>样本集 </p></td> 
  <td class="stentry"> <p>一组项，包括对图像记录的引用和对用作样本的图像记录的可选单独引用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>层次样本集 </p></td> 
  <td class="stentry"> <p>由基本色板项或对色板集记录的引用组成的一组项。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>旋转集 </p></td> 
  <td class="stentry"> <p>由简单的图像ID列表组成的一组项目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>二维旋转集 </p></td> 
  <td class="stentry"> <p>由简单图像或对基本旋转集的引用组成的一组项目。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>页面集 </p></td> 
  <td class="stentry"> <p>一组项目，由最多三幅页面图像的列表组成 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒体集 </p></td> 
  <td class="stentry"> <p>由简单图像、视频集、样本集、分层样本集、旋转集、二维旋转集、页面集和视频资产组成的一组项目。 每个媒体集项目也可包含可选色板。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>视频集 </p></td> 
  <td class="stentry"> <p>由一列表简单视频组成的一组项目。 </p></td> 
 </tr> 
</table>

## 外置式检测 {#section-3dd6e453528d46898e559d31458a59ba}

当接 `req=set` 收请求时，生成的响应类型由值确定 `catalog::AssetType`。 如果 `catalog::AssetType` 未定义，则响应类型由以下规则确定：

* 如果在图像目录中找到记录，则定义 `catalog::ImageSet` 了AND

   * 如果记录图像集字段中的至少一个条目包含冒号，则假定电子目录集
   * 如果记录图像集字段中的至少一个条目包含两个半冒号，则假定已设置媒体。
   * 如果记录图像集字段中的至少一个条目包含一个分号，则假定图像集。
   * 如果没有条目包含冒号或分号，但至少有一个条目包含引用集或内联集（这是2D旋转集），则假定旋转集。
   * 如果没有条目包含冒号、分号或引用集或行内集(即以逗号分隔的图像列表)，则假定未知集。

* 如果在图像和静态内容目录中都找到记录

   * 如果文件扩展名位于以下组合中，则假定为视频：mp3, mp4, flv, f4v,swf, xml
   * 假定图像

* 如果在静态内容目录中找到记录，但在图像目录中找不到记录

   * 如果文件扩展名位于以下组合中，则假定为视频：mp3, mp4, flv, f4v,swf, xml
   * 假定为静态，否则为静态

* 如果在图像目录中找到记录，但在静态内容目录中找不到记录

   * 假设图像

* 如果在图像目录中找不到记录，而在静态内容目录中找不到记录

   * 如果文件扩展名在以下集合中，则假定基于文件的视频：mp3, mp4, flv, f4v,swf, xml
   * 假定基于文件的图像

在所有情况下，生成的xml响应都将符合指定的XML文档，其设置的根节点与检测到的类型相对应。

## 内置式检测 {#section-8f46490e467247e69ce284704def06f3}

当检测到外部集合为类型媒体集时，响应将包含一组与中的每个媒体集条目相对应的媒体集项目 `catalog::ImageSet`。 如果为特定媒体集条目指定了可选类型参数，则该参数将根据下表映射到输出类型：

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

修饰 `labelkey=` 符与字段一起使用， `catalog::UserData`为图像和色板生成标签。 该 `catalog:UserData` 字段被解析为一组键／值对，并且该组中的标签键索引用于检索给定键的值。 然后，在和的属 *`l`* 性中返回此 *`s`* 值 *`i`*。

## 强制限制 {#section-b9f042873bee45a5ae11b69fd42f2bca}

为了限制响应的大小并防止自引用问题，最大嵌套深度由服务器属性控制 `PS::fvctx.nestingLimit`。 如果超出此限制，则返回错误。

为了限制大型电子目录集的xml响应的大小，根据服务器属性禁止小册子集项目的专用元数据 `PS::fvctx.brochureLimit`。 与宣传册相关的所有专用元数据都将导出，直到达到宣传册限制。 一旦超出限制，专用地图和用户数据将被禁止，并且将设置相应的标志以指示禁止了哪种类型的数据。

不支持嵌套媒体集。 嵌套媒体集定义为包含媒体集类型的媒体集项的媒体集。 如果检测到此情况，则将返回错误。

## 示例 {#section-588c9d33aa05482c86cd2b1936887228}

有关请求的XML响应示 `req=set` 例，请参阅“HTML示例”标题下的“属性”页。

`http://crc.scene7.com/is-docs/examples/properties.htm`

## 另请参阅 {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , imageset= [, catalog:::ImageSet](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md)[Image Catalog Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

