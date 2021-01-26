---
description: 图像和SVG数据文件中可识别以下字段。
seo-description: 图像和SVG数据文件中可识别以下字段。
seo-title: 图像_SVG数据
solution: Experience Manager
title: 图像_SVG数据
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6f9595b3-d448-4aa1-87fe-edddfdd48873
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# Image_SVG数据{#image-svg-data}

图像和SVG数据文件中可识别以下字段。

## 目录管理{#section-1056bcc3b6d04166b3aa6ec48913b6b2}

<table id="table_823F89CAD494441690D28F18005F774C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md" type="reference" format="dita" scope="local"> ID</a></span> </p> </td> 
   <td colname="col2"> <p>目录记录标识符（索引键）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 请求属性{#section-cfe69bcdcd4b4d129e99d11b9078ae4a}

<table id="table_C070C676835F49918E1B3BBF81471B09"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba" type="reference" format="dita" scope="local"> DigimarcInfo</a></span> </p> </td> 
   <td colname="col2"> <p>Digimarc嵌入的图像特定信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a" type="reference" format="dita" scope="local"> 过期</a></span> </p> </td> 
   <td colname="col2"> <p>回复图像的缓存过期（停留时间）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md" type="reference" format="dita" scope="local"> 修饰符</a> </span> </p> </td> 
   <td colname="col2"> <p>前缀请求修饰符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md" type="reference" format="dita" scope="local"> PostModifier</a> </span> </p> </td> 
   <td colname="col2"> <p>后缀请求修饰符。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded" type="reference" format="dita" scope="local"> 时间戳</a></span> </p> </td> 
   <td colname="col2"> <p>文件修改时间戳。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 图像属性{#section-74c4d124255d4218ade87d7d1677c76d}

<table id="table_F2A33C2EB17A4EACB00DDEF7FB1BB0D4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md" type="reference" format="dita" scope="local"> 锚点</a></span> </p> </td> 
   <td colname="col2"> <p>图像锚点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md" type="reference" format="dita" scope="local"> 蒙版路径</a></span> </p> </td> 
   <td colname="col2"> <p>遮罩文件路径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md" type="reference" format="dita" scope="local"> 路径</a></span> </p> </td> 
   <td colname="col2"> <p>图像/SVG文件路径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5" type="reference" format="dita" scope="local"> 打印分辨率</a></span> </p> </td> 
   <td colname="col2"> <p>打印分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1" type="reference" format="dita" scope="local"> 分辨率</a></span> </p> </td> 
   <td colname="col2"> <p>对象分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-size-cat.md" type="reference" format="dita" scope="local"> 大小</a></span> </p> </td> 
   <td colname="col2"> <p>图像大小. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 缩略图属性{#section-c5ac27bcd4224a80b7f42ead249027b1}

<table id="table_E07909B6C16F4D9686ADA381A4178E25"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69" type="reference" format="dita" scope="local"> ThumbRes</a></span> </p> </td> 
   <td colname="col2"> <p>缩略图分辨率。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03" type="reference" format="dita" scope="local"> ThumbType</a></span> </p> </td> 
   <td colname="col2"> <p>缩略图类型。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 辅助数据{#section-bff4e1f9af9d45f1872abac3b414a629}

<table id="table_B6A9A702F533494E85CEC1AD42EC728A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-assettype-cat.md" type="reference" format="dita" scope="local"> 资产类型</a></span> </p> </td> 
   <td colname="col2"> <p>资源类型. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md" type="reference" format="dita" scope="local"> 图像集</a></span> </p> </td> 
   <td colname="col2"> <p>图像集数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md" type="reference" format="dita" scope="local"> 地图</a></span> </p> </td> 
   <td colname="col2"> <p>图像映射数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md" type="reference" format="dita" scope="local"> 目标</a></span> </p> </td> 
   <td colname="col2"> <p>缩放目标数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md" type="reference" format="dita" scope="local"> 用户数据</a></span> </p> </td> 
   <td colname="col2"> <p>用户定义的数据。 </p> </td> 
  </tr> 
 </tbody> 
</table>

