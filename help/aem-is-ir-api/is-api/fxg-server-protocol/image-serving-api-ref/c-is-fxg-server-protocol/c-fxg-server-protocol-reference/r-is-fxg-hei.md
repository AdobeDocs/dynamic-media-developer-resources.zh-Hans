---
description: 檢視高度。 指定回覆影像的高度。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# hei{#hei}

檢視高度。 指定回覆影像的高度。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>以畫素為單位的影像高度（整數大於0）。 </p></td> 
 </tr> 
</table>

點陣化格式會使用「預設檢視大小」（或DefaultPix設定）呈現。 按一下 **[!UICONTROL 應用程式設定]** > **[!UICONTROL 發佈設定]** > **[!UICONTROL 影像伺服器]**，然後輸入您的「寬度」和「高度」值。 尺寸越小，效能越高。 您必須儲存設定並執行影像伺服發佈才能套用變更。

如果您套用 `scale=1` 指令，點陣格式要求會以FXG中指定的大小呈現。

## 默认 {#section-76ee3daa77cb468ab310821357cc9404}

如果兩者都不 `wid=`， `hei=`，也不 `scale=` 指定，回覆影像為FXG檔案中指定的預設檢視大小。

## 示例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

除非指定格式，否則影像會呈現為SWF檔案。 在這種情況下，高度和寬度沒有意義，因為SWF通常會展開到瀏覽器視窗的大小。 因此，hei和wid僅適用於點陣或PDF格式。 點陣格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIFalpha
* TIF-alpha
* PNG-alpha
