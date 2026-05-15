---
title: InteractiveSwatches.scrollstep
description: 交互式视频查看器的配置属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
TQID: 'https://experienceleague.adobe.com/28KSiSs54nPSMOpQm7thVn5We8EBvmyAN-YHQB-aITA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 4%

---

# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

交互式视频查看器的配置属性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`步骤`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">步骤</span></span> </p> </td> 
   <td colname="col2"> <p>指定每次点按相应的滚动按钮时所滚动的样本数。 </p> <p>如果指定的值大于可见的交互式样本数，则每次点按都只滚动可见样本数，以防止遗漏任何样本。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-1e637b22e8a44d759d588e47576891e6}

可选.

## 默认 {#section-71fb773f814649b2885aefee68073641}

`3`

## 示例： {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```
