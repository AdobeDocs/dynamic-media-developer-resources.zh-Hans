---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 690aed79-c242-402d-86c0-470a91fbb034
TQID: 'https://experienceleague.adobe.com/KfPe-nLxrVewVf8vLlRwKOBAi7RXVwtiZzTqRRahzLM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 4%

---

# PageView.fmt{#pageview-fmt}

[!DNL `[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 指定组件从图像服务器加载图像时使用的图像格式。 如果指定的格式以<span class="codeph"> -alpha</span>结尾，则组件会将图像渲染为透明内容。 对于所有其他图像格式，组件会将图像视为不透明。 默认情况下，该组件具有白色背景。 因此，若要使其透明，请将<span class="codeph"> background-color</span> CSS属性设置为<span class="codeph"> transparent</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-12a6fb2fcbc1476b95bd53ce880dc185}

可选.

## 默认 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## 示例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]

