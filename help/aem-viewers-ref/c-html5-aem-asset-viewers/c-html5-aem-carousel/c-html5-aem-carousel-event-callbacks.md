---
description: 事件回调
solution: Experience Manager
title: 事件回调
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,User
exl-id: e87b2a84-735c-4412-a4dd-97b18474a1d2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---

# 事件回调{#event-callbacks}

查看器支持网页用于跟踪查看器初始化过程或运行时行为的JavaScript事件回调。

在查看器的构造函数中，通过将事件名称和具有`handlers`属性的相应处理程序函数传递到`config` JSON对象，来分配回调处理程序。 或者，也可以使用`setHandlers()` API方法。

支持的查看器事件包括：

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>查看器事件 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete  </span> </p> </td> 
   <td colname="col2"> <p>查看器初始化完成并创建所有内部组件时触发，以便能够使用<span class="codeph"> getComponent()</span> API。 回调处理程序不接受任何参数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> 每当查看器内发生事件时触发，事件可由事件跟踪系统(如Adobe Analytics)处理。 回调处理程序接受以下参数： </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String} - </span> 当前未使用。 </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String}  </span>  — 当前未使用。 </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String} - </span> 触发事件的查看器SDK组件的实例名称。 </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> 时间戳{Number}  </span>  — 事件时间戳。 </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String} — 事 </span> 件有效负载。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate  </span> </p> </td> 
   <td colname="col2"> <p> 当用户激活与其关联的概览数据热点时触发。 回调处理程序采用以下参数： </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> 数据{对象}  </span>  — 一个JSON对象，其中包含来自热点定义的数据。字段<span class="codeph"> sku </span>是必填字段，而其他字段是可选字段，具体取决于源热点定义。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

另请参阅[CarouselViewer**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-carouselviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)和[setHandlers**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
