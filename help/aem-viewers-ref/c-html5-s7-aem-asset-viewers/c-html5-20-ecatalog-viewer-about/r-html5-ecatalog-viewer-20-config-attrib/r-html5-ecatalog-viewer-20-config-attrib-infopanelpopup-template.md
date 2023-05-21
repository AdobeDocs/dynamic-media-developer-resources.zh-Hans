---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 3%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`模板`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 模板</span></span> </p> </td> 
   <td> <p>從資訊伺服器傳回的資料所要合併到的內容範本。 </p> <p>內容範本是遵循此DTD的XML： </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>內容範本的實際語法如下： </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>也就是說，範本的開頭必須是 <span class="codeph"> &lt;info&gt;</span> 可能包含選擇性預設值的元素 <span class="codeph"> &lt;var&gt;</span> 元素。 範本內容本身， <span class="codeph"> TEMPLATE_CONTENT</span> 是HTML文字。 此外，內容範本可包含括在中的變數名稱 <span class="codeph"> $</span> 以資訊伺服器傳回的變數值或預設值取代的字元。 </p> <p>範本中定義的預設變數可以是全域（如果未設定滑鼠指向效果屬性）或特定滑鼠指向效果索引鍵（如果有滑鼠指向效果屬性）。 </p> <p>在範本處理期間，專用於滑鼠指向鍵的變數會優先於全域變數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>當您設定資訊面板彈出式視窗時，傳遞至資訊面板的HTML代碼和JavaScript代碼會在使用者端電腦上執行。 因此，請確定此類HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-6dd7785357d740d095fa9f7fd0f67da4}

可选.

## 默认 {#section-cd5db06d08aa4de49e37d6c938b41570}

无。

## 示例 {#section-16d184665c484964af9a22f79ff3f840}

假設資訊伺服器回應傳回產品名稱作為變數 `$1$` 和產品影像URL傳回為變數 `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
