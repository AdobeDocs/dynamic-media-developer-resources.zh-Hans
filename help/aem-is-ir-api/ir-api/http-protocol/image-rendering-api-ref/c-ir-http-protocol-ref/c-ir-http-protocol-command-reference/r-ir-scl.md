---
description: 缩放视图。 相对于全分辨率暗角，按指定的缩放因子缩放渲染的图像。
seo-description: 缩放视图。 相对于全分辨率暗角，按指定的缩放因子缩放渲染的图像。
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# scl{#scl}

缩放视图。 相对于全分辨率暗角，按指定的缩放因子缩放渲染的图像。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span></span> </p></td> 
  <td class="stentry"> <p>反比例因子（实数、1.0或更大）。 </p></td> 
 </tr> 
</table>

如 `scl=` 果URL后 `wid=` 面或 `hei=` URL中出现，则会取消这些命令，并 `scl=` 定义服务器返回的图像大小。

但是，如 `wid=` 果URL中 `hei=` 或之后 `scl=` 出现，它们将取消并 `scl=` / `wid=``hei=` 定义服务器返回的图像的大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于，则返回错误 `attribute::MaxPix`。

## 属性 {#section-170458cbd6984bd59a3434431258b20f}

可能发生在请求内的任何位置。 如果在命 `wid=` 令序 `hei=` 列中出现 `scl=` 或出现在之后，则忽略。

调整图像大小 `scl=` 不会更改嵌入在响应图像中的打印分辨率值。

## 默认 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

如果既 `wid=`未指定 `hei=` 也未指定 `scl=` ，则缩放回复图像以适合由定义的大小 `attribute::DefaultPix`。 如 `attribute::DefaultPix` 果为空，则回复图像的大小与暗角的视图图像相同。

## 另请参阅 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [Mode=attribute:::MaxPix](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)[Attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
