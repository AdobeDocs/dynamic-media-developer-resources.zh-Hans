---
title: InteractiveSwatches.maxloadradius
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
TQID: 'https://experienceleague.adobe.com/BhsXOdgu2cCLX9hJEzn6PgW-aRjAZUybM4c891T7gZs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 4%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

交互式视频查看器的配置属性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> 指定组件预载行为。 </p> <p>当设置为<span class="codeph"> -1</span>时，在初始化组件或更改资产时，将同时加载所有样本。 </p> <p>当设置为<span class="codeph"> 0</span>时，将只加载可见的样本。 </p> <p>设置为<span class="codeph"><span class="varname"> preloadnbr</span></span>以定义可见区域周围预载多少不可见的行/列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`1`

## 示例： {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
