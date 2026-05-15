---
title: hei
description: 视图高度。 指定回复图像的高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 1%

---

# hei{#hei}

视图高度。 指定回复图像的高度。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span></span> </p> </td> 
  <td class="stentry"> <p>图像高度，以像素为单位（int大于0）。 </p></td> 
 </tr> 
</table>

栅格格式使用“默认视图大小”（或DefaultPix设置）渲染。 选择&#x200B;**[!UICONTROL 应用程序设置]** > **[!UICONTROL 发布设置]** > **[!UICONTROL 图像服务器]**，然后输入宽度和高度值。 尺寸越小，性能越高。 保存设置并执行图像服务发布以应用更改。

如果应用`scale=1`命令，则栅格格式请求将以FXG中指定的大小呈现。

## 默认 {#section-76ee3daa77cb468ab310821357cc9404}

如果未指定`wid=`、`hei=`或`scale=`，则回复图像是FXG文件中指定的默认视图大小。

## 示例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

除非指定格式，否则图像将渲染为SWF文件。 在这种情况下，高度和宽度没有意义，因为SWF通常会扩展到浏览器窗口的大小。 因此，其和wid仅适用于光栅或PDF格式。 栅格格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alph
* tif-alpha
* png-alpha
