---
description: 视图背景颜色。 指定复合图像(视图图像)的背景颜色。
seo-description: 视图背景颜色。 指定复合图像(视图图像)的背景颜色。
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 3ea8291e-3223-45ff-a2ad-43fc212eff90
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

视图背景颜色。 指定复合图像(视图图像)的背景颜色。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 颜色</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK颜色值。 </p></td> 
 </tr> 
</table>

指定用于视图背景的不透明填充颜色。 仅当复合图像具有透明区域或复合图像具有与视图矩形不同的长宽比时才可见。 如果、 `fmt=tif-alpha` 或 `fmt=png-alpha`，则忽略 `req=mask`。

>[!NOTE]
>
>“s”颜色后缀被忽略 `bgc=`。 使用指定的颜色 `bgc=` 值始终与相应的输出色彩空间相关联。

## 属性 {#section-b729b50b1ea7433b82ba34ecd61839cd}

视图属性。 无论当前图层设置如何，均可应用。 如果、 `req=mask`、 `fmt=tif-alpha`、 `fmt=png-alpha`或，则 `fmt=gif-alpha`忽略 `fmt=swf-alpha`。

将忽略用颜色指定的任何Alpha值。

*`color`* 假定属于输出色彩空间(如指定 `icc=`)，并且应具有与输出图像相同的像素类型。 如果像素类型不匹配，则使用 *`color`* 天真的转换进行转换。

## 默认 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 示例 {#section-7bcdfbc0e1274e86a69d39186b090789}

为缩略图请求指定显式背景颜色：

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 另请参阅 {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),:::BkgColor [,fmt=req=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8)，属性icc [=color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)[，色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
