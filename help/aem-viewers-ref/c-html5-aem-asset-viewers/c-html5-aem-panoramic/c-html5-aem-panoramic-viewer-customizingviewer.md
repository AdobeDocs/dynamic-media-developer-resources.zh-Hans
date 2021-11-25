---
title: 自定义全景查看器
description: 全景查看器的所有可视化自定义和大多数行为自定义都是通过创建自定义CSS来完成的。
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

所有可视化自定义和大多数行为自定义都是通过创建自定义CSS来完成的。

建议的工作流是为相应的查看器获取默认的CSS文件，将其复制到其他位置，自定义它，并在 `style=` 命令。

默认CSS文件可在以下位置找到：

`<s7viewers_root>/html5/PanoramicViewer.css`

自定义CSS文件必须包含与默认类声明相同的类声明。 如果忽略类声明，则查看器将无法正常运行，因为它不为用户界面元素提供内置的默认样式。

提供自定义CSS规则的替代方法是，直接在网页或某个链接的外部CSS规则中使用嵌入的样式。

创建自定义CSS时，请记住查看器分配 `.s7panoramicviewer` 类添加到其容器DOM元素。 如果您使用的是通过 `style=` 命令，使用 `.s7panoramicviewer` 类作为CSS规则的子选择器中的父类。 如果您在网页上执行嵌入的样式，则此外，还应使用容器DOM元素的ID来限定此选择器，如下所示：

`#<containerId>.s7panoramicviewer.`


## 一般样式说明和建议 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS中指向外部资产的所有路径都将根据CSS位置进行解析，而不是根据查看器HTML页面位置进行解析。 将默认CSS复制到其他位置时，请考虑这一点：可能需要复制默认资产或更新自定义CSS中的路径。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明， `rgba(R,G,B,A)` 格式。 否则，不需要透明度 `#RRGGBB` 中。

使用CSS自定义查看器UI时，使用 `!IMPORTANT` 样式查看器元素不支持规则。 特别是， `!IMPORTANT` 规则不应用于覆盖查看器或查看器SDK提供的任何默认或运行时样式，因为它可能会影响正确的组件行为。 相反，应使用具有适当特性的CSS选择器来设置本参考指南中介绍的CSS属性。

## 全景查看器CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**主查看器区域**
主视区是全景图像所占用的区域。  通常在未指定大小时设置为适合可用设备屏幕。

通过CSS类选择器控制查看区域的外观：
`.s7panoramicviewer`

适用的CSS属性包括：

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 查看者的宽度； </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 观看者的身高； </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
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
