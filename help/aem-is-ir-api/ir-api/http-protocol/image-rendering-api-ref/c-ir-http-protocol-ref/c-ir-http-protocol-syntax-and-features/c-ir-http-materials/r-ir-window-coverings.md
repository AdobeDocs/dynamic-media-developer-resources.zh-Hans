---
description: 窗帘材料包括软窗帘（窗帘、窗帘、咖啡窗帘）和硬窗帘（窗帘和百叶窗）。
solution: Experience Manager
title: 窗盖
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---


# 窗口覆盖{#window-coverings}

窗帘材料包括软窗帘（窗帘、窗帘、咖啡窗帘）和硬窗帘（窗帘和百叶窗）。

窗口覆盖材料指定一个&#x200B;*窗口覆盖样式文件*（[!DNL .vnw]文件扩展名），一个类似于晕影的特殊数据文件，包含定义窗口覆盖的蒙版、照明、布局和纹理化数据。

[!DNL vnw] 文件不包括用于窗口覆盖的颜色和纹理（结构）。此信息是单独指定的，类似于可重复的纹理。

窗口覆盖材料只能应用于“窗口覆盖框架对象”（即重叠对象）。

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
   <th colname="col3" class="entry"> <p>默认 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>窗口覆盖样式文件；。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>纹理图像文件（<span class="codeph"> src= </span>的第二个值）。 </p> </td> 
   <td colname="col3"> <p>无。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>纹理分辨率。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 属性：:Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> 重复=  </span> </a> </p> </td> 
   <td colname="col2"> <p>重复模式。 </p> </td> 
   <td colname="col3"> <p>0（直重复） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>纯色（或着色纹理）。 </p> </td> 
   <td colname="col3"> <p>128（中灰色） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>锐化. </p> </td> 
   <td colname="col3"> <p>0（无锐化） </p> </td> 
  </tr> 
 </tbody> 
</table>

