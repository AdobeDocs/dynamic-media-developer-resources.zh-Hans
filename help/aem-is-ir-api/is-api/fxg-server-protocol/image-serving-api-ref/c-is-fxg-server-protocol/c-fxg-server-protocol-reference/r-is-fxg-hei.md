---
description: 视图高度。 指定回复图像的高度。
seo-description: 视图高度。 指定回复图像的高度。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

视图高度。 指定回复图像的高度。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>图像高度（以像素为单位）（大于0的整数）。 </p></td> 
 </tr> 
</table>

栅格格式使用“默认视图大小”（或“DefaultPix”设置）进行渲染。 单击“ **[!UICONTROL 应用程序设置]** ”>“发布设置 **[!UICONTROL ”]** >“图 **[!UICONTROL 像服务器”]**，然后输入“宽度”和“高度”值。 较小的尺寸可提供更好的性能。 您必须保存设置并执行图像服务发布才能应用更改。

如果应用命令， `scale=1` 则栅格格式请求将以FXG中指定的大小呈现。

## 默认 {#section-76ee3daa77cb468ab310821357cc9404}

如果既 `wid=`未指定 `hei=`、也未指 `scale=` 定，则返回图像是FXG文件中指定的默认视图大小。

## 示例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

除非指定格式，否则图像将呈现为SWF文件。 在这种情况下，高度和宽度没有意义，因为SWF通常会扩展到浏览器窗口的大小。 因此，hei和wid仅适用于栅格或PDF格式。 栅格格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

