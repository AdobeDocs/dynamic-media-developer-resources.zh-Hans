---
title: bgc
description: 查看背景颜色。 指定复合图像（视图图像）的背景颜色。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39ca0d63-55c6-40be-88b6-cf73828cc355
TQID: 'https://experienceleague.adobe.com/XE6I3hjg95AVJYiszVOlRsn19YSA3bhomHNxJlFmVDs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 2%

---

# bgc{#bgc}

查看背景颜色。 指定复合图像（视图图像）的背景颜色。

`bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">颜色</span></span> </p> </td> 
  <td class="stentry"> <p>灰色、RGB或CMYK颜色值。 </p></td> 
 </tr> 
</table>

指定用于视图背景的不透明填充颜色。 仅当复合图像具有透明区域或复合图像的纵横比不同于视图矩形时才可见。 已忽略`fmt=tif-alpha`、`fmt=png-alpha`或`req=mask`。

>[!NOTE]
>
>`bgc=`忽略了“s”颜色后缀。 使用`bgc=`指定的颜色值始终与相应的输出颜色空间关联。

## 属性 {#section-b729b50b1ea7433b82ba34ecd61839cd}

查看属性。 无论当前图层设置如何，均适用。 已忽略`req=mask`、`fmt=tif-alpha`、`fmt=png-alpha`、`fmt=gif-alpha`或`fmt=swf-alpha`。

将忽略通过颜色指定的任何alpha值。

假设&#x200B;*`color`*&#x200B;属于输出颜色空间（如`icc=`所指定），并且像素类型应与输出图像相同。 如果像素类型不匹配，则使用朴素转换来转换&#x200B;*`color`*。

## 默认 {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## 示例 {#section-7bcdfbc0e1274e86a69d39186b090789}

为缩略图请求指定明确的背景颜色：

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## 另请参阅 {#section-1e55f9f98f1847918a1725836a27cfaa}

[颜色](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93)，[属性：：BkgColor](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8)，[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)，[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)，[icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)，[色彩管理](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
