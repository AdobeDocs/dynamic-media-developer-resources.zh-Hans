---
description: 有助于提高优化金字塔TIF文件图像锐度的设置。
solution: Experience Manager
title: UnsharpMaskOptions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 7150b4a8-a44d-4858-96f2-6004d5f48e77
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 11%

---

# [!DNL UnsharpMaskOptions]{#unsharpmaskoptions}

有助于提高优化金字塔TIF文件图像锐度的设置。

`unsharpMaskOptions=[ *`数量，半径，阈值，单色`*]`

## 参数 {#section-c3f0d03136ba4422819cb463bd393885}

为带有`unsharpMaskOptions`n`minOccurs=" *`的`*".`选项指定一个值

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
   <td colname="col3"><p>控制应用于边缘像素的对比度。 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">范围：0.0 - 5.0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">默认：0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 半径</span></span></td>
   <td colname="col2"><span class="codeph"> xsd：double</span></td>
   <td colname="col3"><p>通过设置图像边缘周围的像素数来控制锐度。 值正确与否取决于图像的大小。 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">范围：0.0 - 250.0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">低值仅锐化边缘像素。 </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">高值会锐化较宽的像素范围。 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 阀值</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>确定不同的像素与周围区域必须有多大的差异，才会被视为边缘像素并且可以锐化。 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">范围：0 - 255（仅限整数）。 </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">默认值：6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 单色</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>值仅包括<span class="codeph"> 0</span>或<span class="codeph"> 1</span>。 </p><p>设置为<span class="codeph"> 0</span>将分别应用至每个颜色组件，或者设置为<span class="codeph"> 1</span>将仅应用至图像亮度（强度）。 图层蒙版或复合蒙版也被锐化。 </p><p>对灰度图像忽略<span class="codeph"><span class="varname">单色</span></span>。 </p></td>
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

`unsharpMaskOptions`类型由以下用户使用：

* [重新处理资产作业](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [上载目录作业](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [图像服务API引用：op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html?lang=zh-Hans)
