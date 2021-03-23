---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
uuid: c7063907-78e8-47f8-9424-78ab9d123ad1
feature: Dynamic Media Classic，查看器，SDK/API，电子目录
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`模板`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 模板</span></span> </p> </td> 
   <td> <p>从信息服务器返回的数据合并到的内容模板。 </p> <p>内容模板是遵循此DTD的XML: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>内容模板的实际语法如下： </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>也就是说，模板必须与<span class="codeph"> &lt;info&gt;</span>元素进行开始，该元素可能包含可选的默认<span class="codeph"> &lt;var&gt;</span>元素。 模板内容本身<span class="codeph"> TEMPLATE_CONTENT</span>是HTML文本。 此外，内容模板可能包含包含在<span class="codeph"> $</span>字符中的变量名，这些变量名将替换为信息服务器返回的变量值或默认值。 </p> <p>在模板中定义的默认变量可以是全局（如果未设置翻转属性）或特定于某个翻转键（如果存在翻转属性）。 </p> <p>在模板处理过程中，特定于滚动键的变量优先于全局变量。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>请注意，配置“信息面板弹出窗口”时，传递给“信息面板”的HTML代码和JavaScript代码在客户端的计算机上运行。 因此，请确保此类HTML代码和JavaScript代码是安全的。

## 属性 {#section-6dd7785357d740d095fa9f7fd0f67da4}

可选。

## 默认 {#section-cd5db06d08aa4de49e37d6c938b41570}

无。

## 示例 {#section-16d184665c484964af9a22f79ff3f840}

假定信息服务器响应将产品名称返回为变量`$1$`，产品图像URL返回为变量`$2$`。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
