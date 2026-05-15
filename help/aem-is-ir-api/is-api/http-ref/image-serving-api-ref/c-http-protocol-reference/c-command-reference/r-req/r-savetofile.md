---
description: 将图像保存到文件。
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
TQID: 'https://experienceleague.adobe.com/6JtqM7IKcYInFZ4zyuAIVwOabdXIltB2ZsVZP6pLL4E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 1%

---

# saveToFile{#savetofile}

将图像保存到文件。

`req=saveToFile&name= *`文件`*[&timeout= *`值`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">文件</span> </p> </td> 
  <td class="stentry"> <p>目标图像文件的相对路径。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p></td> 
  <td class="stentry"> <p>超时间隔（毫秒）。 </p></td> 
 </tr> 
</table>

将响应图像保存到服务器上的文件，而不是将其返回到客户端。

成功完成保存请求后，该请求将返回多个Java格式属性，其中包括：

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>属性</b> </th> 
   <th class="entry"> <b>类型</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">上次更新时间</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>文件创建时间（自午夜1970 UTC/GMT年1月1日以来的毫秒数）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">像素总计</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> 已保存图像中的像素数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph">状态</span> </p> </td> 
   <td> <p> 枚举 </p> </td> 
   <td> <p> 如果成功，<span class="codeph">完成</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果成功，则返回HTTP响应状态200；如果请求失败或超时，则返回403。 响应具有MIME类型`text/plain`且不可缓存。

重要信息必须通过指定`attribute::SavePath`中现有可写文件夹的路径来启用保存到文件。 如果`attribute::SavePath`为空，`saveToFile=`将失败。

*`file`*&#x200B;是必需的，并且必须是与`attribute::SavePath`组合的相对路径。 图像服务不会创建文件夹。 目标文件夹必须存在于服务器上，并且具有适当的权限设置，图像服务才能创建文件。

`timeout=`是可选的。 默认超时为60,000毫秒，或者使用`PS::SaveTimeout`配置的值。
