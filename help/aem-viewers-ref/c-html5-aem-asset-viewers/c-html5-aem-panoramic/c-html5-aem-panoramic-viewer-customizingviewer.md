---
title: 自定义全景查看器
description: 全景查看器的所有可视化自定义和大多数行为自定义均通过创建自定义CSS来完成。
keywords: 响应式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# 自定义Video360查看器{#customizing-video-viewer}

所有可视化自定义和大多数行为自定义均通过创建自定义CSS来完成。

建议的工作流程是获取相应查看器的默认CSS文件，将其复制到其他位置，对其进行自定义，然后在 `style=` 命令。

可以在以下位置找到默认CSS文件：

`<s7viewers_root>/html5/PanoramicViewer.css`

自定义CSS文件必须包含与默认文件相同的类声明。 如果省略类声明，则查看器将无法正常运行，因为它没有为用户界面元素提供内置的默认样式。

提供自定义CSS规则的替代方法是直接在网页上或某个链接的外部CSS规则中使用嵌入样式。

创建自定义CSS时，请记住查看器分配 `.s7panoramicviewer` 类到其容器DOM元素。 如果您使用传递的外部CSS文件 `style=` 命令，使用 `.s7panoramicviewer` 类作为CSS规则的后代选择器中的父类。 如果您在网页上执行嵌入样式，则另外请使用容器DOM元素的ID来限定此选择器，如下所示：

`#<containerId>.s7panoramicviewer.`


## 一般样式注释和建议 {#section-95855dccbbc444e79970f1aaa3260b7b}

* 指向CSS内外部资源的所有路径都是针对CSS位置解析的，而不是针对查看器HTML页面位置解析的。 将默认CSS复制到其他位置时，请考虑这一点：可能也需要复制默认资产或更新自定义CSS中的路径。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度， `rgba(R,G,B,A)` 建议使用格式。 否则，不需要透明度 `#RRGGBB` 可以使用。

使用CSS自定义查看器UI时，请使用 `!IMPORTANT` 样式查看器元素不支持规则。 特别是， `!IMPORTANT` 规则不应用于覆盖查看器或查看器SDK提供的任何默认样式或运行时样式，因为它可能会影响正确的组件行为。 相反，应使用具有适当特定性的CSS选择器来设置本参考指南中记录的CSS属性。

## 全景查看器CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**主查看器区域**
主视图区域是全景图像所占用的区域。  当未指定大小时，它通常设置为适合可用的设备屏幕。

查看区域的外观由CSS类选择器控制：
`.s7panoramicviewer`

适用的CSS属性包括：

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 查看器的宽度； </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 观看者的高度； </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

示例：设置大小为1024 x 512像素的查看器。

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**全景视图**
主视图由全景图像组成。

主视图的外观由CSS类选择器控制：
`.s7panoramicviewer .s7panoramicview`

适用的CSS属性包括：
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 主视图的背景颜色； </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

示例：要使主视图透明，请执行以下操作：

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
