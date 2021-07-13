---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic，查看器，SDK/API，eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`模板`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 模板</span></span> </p> </td> 
   <td> <p>从信息服务器返回的数据将合并到的内容模板。 </p> <p>内容模板是遵循此DTD的XML: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>内容模板的实际语法如下： </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>即，模板必须以<span class="codeph"> &lt;info&gt;</span>元素开头，该元素可能包含可选的默认<span class="codeph"> &lt;var&gt;</span>元素。 模板内容本身<span class="codeph"> TEMPLATE_CONTENT</span>是HTML文本。 此外，内容模板可能包含包含在<span class="codeph"> $</span>字符中的变量名称，这些名称将被信息服务器返回的变量值或默认值替换。 </p> <p>模板中定义的默认变量可以是全局变量（如果未设置滚动更新属性），也可以是特定于特定滚动更新键（如果存在滚动更新属性）。 </p> <p>在模板处理过程中，特定于滚动键的变量优先于全局变量。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>请注意，配置“信息面板弹出窗口”时，传递到“信息面板”的HTML代码和JavaScript代码将在客户端的计算机上运行。 因此，请确保此类HTML代码和JavaScript代码的安全。

## 属性 {#section-6dd7785357d740d095fa9f7fd0f67da4}

可选。

## 默认 {#section-cd5db06d08aa4de49e37d6c938b41570}

无。

## 示例 {#section-16d184665c484964af9a22f79ff3f840}

假定信息服务器响应将产品名称返回为变量`$1$`，产品图像URL返回为变量`$2$`。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
