---
description: 视图高度。 指定回复图像的高度。
seo-description: 视图高度。 指定回复图像的高度。
seo-title: hei
solution: Experience Manager
title: 平
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 4%

---


# hei{#hei}

视图高度。 指定回复图像的高度。

`hei= *`瓦尔`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 瓦尔</span></span> </p> </td> 
  <td class="stentry"> <p>图像高度（以像素为单位，整数大于0）。 </p></td> 
 </tr> 
</table>

栅格格式使用“默认视图大小”（或“DefaultPix”设置）进行渲染。 单击&#x200B;**[!UICONTROL 应用程序设置]** > **[!UICONTROL 发布设置]** > **[!UICONTROL 图像服务器]**，然后输入宽度和高度值。 较小尺寸可提供更好的性能。 要应用更改，必须保存设置并执行图像服务发布。

如果应用`scale=1`命令，将以FXG中指定的大小呈现栅格格式请求。

## 默认 {#section-76ee3daa77cb468ab310821357cc9404}

如果未指定`wid=`、`hei=`和`scale=`，则返回图像是在FXG文件中指定的默认视图大小。

## 示例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

除非指定了格式，否则图像将呈现为SWF文件。 在这种情况下，高度和宽度毫无意义，因为SWF通常会扩展到浏览器窗口的大小。 因此，hei和wid仅应用于栅格格式或PDF格式。 栅格格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-α
* PNG-alpha

