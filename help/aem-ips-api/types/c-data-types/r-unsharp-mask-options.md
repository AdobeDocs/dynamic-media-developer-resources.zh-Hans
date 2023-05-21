---
description: 有助於改善最佳化金字塔TIF檔案之影像銳利度的設定。
solution: Experience Manager
title: 不銳利化遮色片選項
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 7150b4a8-a44d-4858-96f2-6004d5f48e77
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 13%

---

# [!DNL UnsharpMaskOptions]{#unsharpmaskoptions}

有助於改善最佳化金字塔TIF檔案之影像銳利度的設定。

`unsharpMaskOptions=[ *`数量、半径、阈值、单色`*]`

## 参数 {#section-c3f0d03136ba4422819cb463bd393885}

指定值 `unsharpMaskOptions` 選項，搭配 `minOccurs=" *`n`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 名称 </th>
   <th colname="col2" class="entry"> 类型 </th>
   <th colname="col3" class="entry"> 说明 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 数量</span></span></td>
   <td colname="col2"><span class="codeph"> xsd：double</span></td>
   <td colname="col3"><p>控制套用至邊緣畫素的對比。 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">範圍： 0.0 - 5.0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">預設： 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 半徑</span></span></td>
   <td colname="col2"><span class="codeph"> xsd：double</span></td>
   <td colname="col3"><p>藉由設定影像邊緣周圍的畫素數來控制銳利度。 值正确与否取决于图像的大小。 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">範圍： 0.0 - 250.0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">低值只會銳利化邊緣畫素。 </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">高數值會銳利化較寬的畫素範圍。 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 阀值</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>決定畫素與周圍區域必須有多大的差異，才會被視為邊緣畫素，並可加以銳利化。 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">範圍： 0 - 255 （僅限整數）。 </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">預設： 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 單色</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>值包括 <span class="codeph"> 0</span> 或 <span class="codeph"> 1</span> 僅限。 </p><p>設定為 <span class="codeph"> 0</span> 分別套用至每個色彩元件，或套用至 <span class="codeph"> 1</span> 僅套用至影像亮度（強度）。 圖層遮色片或複合遮色片也會銳利化。 </p><p><span class="codeph"><span class="varname"> 單色</span></span> 會略過灰階影像。 </p></td>
  </tr>
 </tbody>
</table>

## 示例 {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## 使用者 {#section-db8124a5468b498694a780f8a56a4560}

此 `unsharpMaskOptions` 型別使用者：

* [重新處理資產工作](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectory作業](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadpostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [影像伺服API參考： op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)

