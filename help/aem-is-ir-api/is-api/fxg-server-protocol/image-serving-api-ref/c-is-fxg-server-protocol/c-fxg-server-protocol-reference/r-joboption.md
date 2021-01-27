---
description: 应用PDF作业选项。 作业选项文件或PDF预设是Illustrator在“另存为PDF选项”对话框或InDesign的PDF预设中生成的文件。
seo-description: 应用PDF作业选项。 作业选项文件或PDF预设是Illustrator在“另存为PDF选项”对话框或InDesign的PDF预设中生成的文件。
seo-title: 作业选项
solution: Experience Manager
title: 作业选项
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7288cf29-850f-4121-8425-5f995daac22d
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 42%

---


# joboption{#joboption}

应用PDF作业选项。 作业选项文件或PDF预设是Illustrator在“另存为PDF选项”对话框或InDesign的PDF预设中生成的文件。

` joboption= *`值`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 值</span></span> </p> </td> 
  <td class="stentry"> <p>作业选项文件的IPSID。 </p></td> 
 </tr> 
</table>

作业选项文件可由IPS/Dynamic Media经典上传和发布。 生成PDF时，将使用作业选项文件中包含的PDF选项。

当前支持以下选项：

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>常规 </p></td> 
  <td class="stentry"> <p> 兼容性 </p> <p> 对象级压缩 </p> <p> 嵌入缩略图 </p> <p> 优化快速 Web 查看 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>图像 </p></td> 
  <td class="stentry"> <p> 缩减像素取样颜色、灰色和单色的分辨率、阈值和压缩 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>字体 </p></td> 
  <td class="stentry"> <p> 嵌入所有字体 </p> <p> 嵌入 OpenType 字体 </p> <p> 子集化嵌入的字体，若被使用的字符百分比低于: </p> <p> 始终嵌入列表 </p> <p> 永不嵌入列表 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>颜色 </p></td> 
  <td class="stentry"> <p> 颜色策略（仅标记图像被视为标记所有内容） </p> <p> 文档渲染方法 </p> <p> 4.2.5 仅支持下列工作空间。 </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB，编码范围为 [-4.0, 4.0] </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> 平面 XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">线性 ROMM-RGB </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC 8 位 </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC 8 位 </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">灰度 <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">灰度系数 1.8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">灰度系数 2.2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">网点增大 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">网点增大 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">网点增大 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> 网点增大 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">网点增大 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> 保留 CMYK 值用于校准的 CMYK 色彩空间 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>高级 </p></td> 
  <td class="stentry"> <p>保留 OPI 注释始终处于打开状态。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>标准 </p></td> 
  <td class="stentry"> <p>合规标准。 </p></td> 
 </tr> 
</table>

