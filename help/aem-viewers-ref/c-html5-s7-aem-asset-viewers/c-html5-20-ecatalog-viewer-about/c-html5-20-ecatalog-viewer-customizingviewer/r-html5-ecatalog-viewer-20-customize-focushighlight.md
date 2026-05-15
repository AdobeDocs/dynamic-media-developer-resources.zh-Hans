---
title: 焦点高亮
description: 焦点查看器用户界面元素周围显示的输入焦点高亮。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5737d7-1295-46a9-9b84-c43269e5a914
TQID: 'https://experienceleague.adobe.com/8xcQUHsvWwaKyz9-UA1cQbFhQmOpfiXGJ4EpERAJJow'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 0%

---

# 焦点高亮{#focus-highlight}

焦点查看器用户界面元素周围显示的输入焦点高亮。

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

焦点高亮显示的外观可通过以下CSS类选择器进行控制：

```
.s7ecatalogviewer *:focus
```

焦点突出显示的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">大纲</span> </p> </td> 
   <td colname="col2"> <p> 焦点突出显示样式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要禁用所有查看器用户界面元素的默认浏览器焦点高亮显示，请将以下CSS选择器添加到查看器的样式表中：

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
