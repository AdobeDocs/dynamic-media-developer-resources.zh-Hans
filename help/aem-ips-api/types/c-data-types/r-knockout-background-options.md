---
title: 去底色背景選項
description: 遮色片（去底色）選取影像的背景。 此資料型別可讓您以主題影像以外的透明度，將之覆蓋在其他圖層中。 選擇性引數，預設為關閉。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 5%

---

# [!DNL KnockoutBackgroundOptions]{#knockoutbackgroundoptions}

遮色片（去底色）選取影像的背景。 此資料型別可讓您以主旨影像以外的透明度，將影像覆蓋在其他圖層中。

此資料型別為選用，預設為關閉。

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## 参数 {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>如果您正在設定 `KnockoutBackgroundOptions` 在Adobe Experience Manager中，請改用下列引數：
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod`
>
>示例: `kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 轉角</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">選取您要使用的轉角。 <span class="codeph"> 轉角</span> 接受這些值： 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> 左上方</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> 左下方</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> 右上方</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> 右下</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 容許度</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3">選擇性設定，可根據透明度從影像邊緣移除空白區域。 接受從0.0到1.0的值範圍。指定： 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0表示完全符合顏色。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1以啟用最大的色彩差異。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 填色方法</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>在指定的位置控制畫素透明度 <span class="codeph"><span class="varname"> 轉角</span></span> 變數。 此 <span class="codeph"> 填色方法</span> 接受這些值： </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>：將指定角落中的所有畫素變成透明。 </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>：將所有相符的畫素變成透明，無論位置為何。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## 使用者 {#section-28c43baafe85434a9ee9e303ed10569a}

此 `KnockoutBackgroundOptions` 型別使用者：

* [UploadDirectory作業](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadpostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
