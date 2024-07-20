---
title: 挖空背景选项
description: 蒙版（去底色）选定图像的背景。 使用此数据类型，您可以将其叠加到其他图层中，并使其在主题图像之外透明。 默认处于关闭状态的可选参数。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed8cf2e-5a09-43ff-9420-0d0d54059515
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# [!DNL KnockoutBackgroundOptions]{#knockoutbackgroundoptions}

蒙版（去底色）选定图像的背景。 使用此数据类型，您可以将其叠加到其他图层中，并使其在主题图像之外透明。

此数据类型是可选的，默认情况下是关闭的。

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## 参数 {#section-3149b49ccb714e6eafa6655354816819}

>[!IMPORTANT]
>
>如果您在Adobe Experience Manager中配置`KnockoutBackgroundOptions`，请改用以下参数：
>* `kbCorner`
>* `kbTolerance`
>* `kbFillMethod`
>
>例如： `kbCorner=UpperLeft&kbTolerance=0.2&kbFillMethod=MatchPixel`

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
   <td colname="col1"> <span class="codeph"> <span class="varname">角</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3">选择要使用的拐角。 <span class="codeph">角</span>接受以下值： 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> 左上</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> 左下方</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> 右上</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> 右下</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">容差</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3">一个可选设置，用于根据透明度从图像边缘中去除空格。 接受从0.0到1.0的值的范围。指定： 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0表示完全匹配颜色。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1启用最大的颜色差异。 </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>控制由<span class="codeph"><span class="varname">角</span></span>变量指定的位置的像素透明度。 <span class="codeph"> fillMethod</span>接受以下值： </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>：将指定角的所有像素变为透明。 </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>：将所有匹配的像素变为透明，不论其位置如何。 </li> 
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

`KnockoutBackgroundOptions`类型由以下用户使用：

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
