---
description: 视图高度。 指定回复图像的高度。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 3%

---

# 平{#hei}

视图高度。 指定回复图像的高度。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>图像高度（以像素为单位，整数大于0）。 </p></td> 
 </tr> 
</table>

栅格格式使用“默认视图大小”（或“默认图像”设置）呈现。 单击&#x200B;**[!UICONTROL 应用程序设置]** > **[!UICONTROL 发布设置]** > **[!UICONTROL 图像服务器]**，然后输入宽度和高度值。 较小的尺寸可提供更好的性能。 您必须保存设置并执行图像提供发布以应用更改。

如果应用`scale=1`命令，将以FXG中指定的大小呈现光栅格式请求。

## 默认 {#section-76ee3daa77cb468ab310821357cc9404}

如果既未指定`wid=`、`hei=`和`scale=`，则回复图像为FXG文件中指定的默认视图大小。

## 示例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

除非指定格式，否则图像将呈现为SWF文件。 在这种情况下，高度和宽度没有任何意义，因为SWF通常会扩展为浏览器窗口的大小。 因此，hei和wid仅适用于光栅格式或PDF格式。 光栅格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-α
* PNG-α
