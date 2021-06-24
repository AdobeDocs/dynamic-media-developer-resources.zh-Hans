---
description: 允许授权导出以前上传的文件的作业类型。
solution: Experience Manager
title: ExportJob
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 16%

---

# ExportJob{#exportjob}

允许授权导出以前上传的文件的作业类型。

ExportJob不支持以下资产类型：

* 图像集
* 渲染集
* 旋转集
* 媒体集
* 多比特率集
* 视频集
* eCatalog
* 优惠套餐

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 类型：HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>需要导出的<span class="codeph"> assetHandle</span>列表。 请参阅<a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>指定<span class="codeph"> export.Possible Values</span>的类型：[原始，转换] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">如果<span class="codeph"> fmt=orig</span>，则资产将作为原始资产导出 </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">如果<span class="codeph"> fmt=convert</span>，则资产将转换为在<span class="codeph"> is_modifer</span>或<span class="codeph">宏</span>输入参数中指定的格式 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>指定<span class="codeph"> ImageServer</span>渲染URL字符串，该字符串将附加到ExportJob <span class="codeph"> convert</span>请求中。 </p> <p>有关发送IS修饰符的详细信息，请参阅<a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/home.html" scope="external" format="html"> IS文档</a>。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 宏</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>选择电子邮件设置。 可能的值︰ </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> 所有</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> 错误</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> 错误和警告</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> 作业完成</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> 无</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>指定启动导出请求的客户或客户的IP地址。 </p> <p> <p>注意： 此参数当前未被主动填充，且严格保留供将来使用。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

对于同时提供`fmt=convert`和`is_modifier`和`macro`的ExportJob请求，目标文件遵循`macro`提供的格式。 例如：

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
