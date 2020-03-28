---
description: 用于根据颜色自动裁剪图像的选项。
seo-description: 用于根据颜色自动裁剪图像的选项。
seo-title: AutoColorCropOptions
solution: Experience Manager
title: AutoColorCropOptions
topic: Scene7 Image Production System API
uuid: 632ae721-7b39-4cd1-a1c6-1a3554167a4e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AutoColorCropOptions{#autocolorcropoptions}

用于根据颜色自动裁剪图像的选项。

语法

## 参数 {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 转角</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 选择“自动裁剪角”。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 容 <span class="varname"> 差</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:多次</span> </td> 
   <td colname="col3">颜色匹配规范。 使用： 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0与颜色完全匹配。 </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1以启用最大的颜色差异。 </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

