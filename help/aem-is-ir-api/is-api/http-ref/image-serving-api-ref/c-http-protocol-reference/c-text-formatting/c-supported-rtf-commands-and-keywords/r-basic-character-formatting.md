---
description: 使用以下命令进行基本字符格式设置。
seo-description: 使用以下命令进行基本字符格式设置。
seo-title: 基本字符格式
solution: Experience Manager
title: 基本字符格式
topic: Scene7 Image Serving - Image Rendering API
uuid: cc8f276a-ebcc-479b-bd86-7ac0dc755f11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 基本字符格式{#basic-character-formatting}

使用以下命令进行基本字符格式设置。

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> 命令 </th> 
   <th class="entry"> 说明 </th> 
   <th class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \纯 </span> </td> 
   <td> <p>将字符格式重置为默认值。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f <span class="varname"> N </span></span> </td> 
   <td> <p>字体。 </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl </span> index </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs <span class="varname"> N </span></span> </td> 
   <td> <p>字体大小. </p> </td> 
   <td> <p>半分；默认值为24。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf <span class="varname"> N </span></span> </td> 
   <td> <p>字体颜色. </p> </td> 
   <td> <p>颜色表中从0开始的索引。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>粗体样式。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i </span> </td> 
   <td> <p>斜体样式。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub </span> </td> 
   <td> <p>下标. </p> </td> 
   <td> <p>减小字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super </span> </td> 
   <td> <p>上标. </p> </td> 
   <td> <p>减小字体大小。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul </span> </td> 
   <td> <p>下划线。 </p> </td> 
   <td> <p>图像服务还可以识别以下RTF下划线命令： </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashd </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ult </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave </span> </li> 
     </ul> </p> <p>这些下划线目前作为标准 <span class="codeph"> \ul下划线 </span> 实现。 忽略所有其他RTF下划线命令。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone </span> </td> 
   <td> <p>关闭下划线 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0 </span> </td> 
   <td> <p>关闭下划线 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \大写字母 </span> </td> 
   <td> <p>大写字母 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps </span> </td> 
   <td> <p>小写（“小型大写”） </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> 仅限。 </p> </td> 
  </tr> 
 </tbody> 
</table>

