---
title: 晕影
description: 晕影是通过Dynamic Media图像创作功能创作的、用于图像渲染的图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# 晕影{#vignettes}

晕影是通过Dynamic Media图像创作功能创作的、用于图像渲染的图像。

IR支持两种基本类型的晕影： *2D* 和 *三维*. 房间场景通常是3D晕影，可以渲染反射，而大多数其他场景，例如服装或室内装饰，通常是不具有反射渲染能力的2D晕影。

晕影包含 *视图* 和层级结构 *对象*.

视图是主图像、共享光照图、共享反射图以及与整个图像关联的其他数据的容器。

对象层次结构包括 *对象组*， *标准对象*、和 *重叠对象*.

每个标准对象控制视图图像的一个区域，该区域用灰度定义 *蒙版*. 标准对象的蒙版从不重叠。 标准对象不能直接隐藏，但它们可能部分或全部被重叠对象覆盖。 典型晕影中的大多数或所有对象都是标准对象。

将对象图层重叠在视图图像之上，并且彼此重叠。 重叠的顺序由指定给对象的z值定义。 当场景的某些部分必须动态显示或隐藏时，重叠对象非常有用。

支持多种类型的对象（包括标准对象和重叠对象），每种对象都有其各自不同的用途：

* **平面对象** （在3D晕影中）和 **平面对象** （在2D晕影中）接受可重复的纹理材料。 它们通常用于地板、工作台面和其他只需要透视映射的平坦曲面。
* **Flowline对象** 绘制形状平滑的曲面，如装饰物，有时也用于服装对象。 它们可以用于2D和3D晕影，并且如果完全创作，可以参与反射渲染。
* **不可纹理的对象** 仅允许颜色更改。 2D和3D晕影均允许使用。 它们或者本身不可纹理，或者它们可以是平面或流线对象，具有特殊的“无纹理”标志设置。 此方法在3D晕影中非常有用，允许对象参与反射渲染，即使对象仅接受纯色材质也是如此。
* **Sketch对象** 最适合用于具有褶皱和皱纹的织物对象，例如服装项目。 与流线对象一样，它们也可以在2D和3D晕影中使用，尽管在3D晕影中的应用是有限的。
* **壁对象** 类似于平面对象，仅在3D晕影中受支持。 它们具有特殊的布局信息，允许应用两种不同的墙面涂饰（上层和下层）和最多三种墙面边界材料。 如果创作得当，应用于墙壁的材料可在相邻墙壁之间准确无缝地流动，用于逼真的壁纸/墙壁边界应用。 壁对象不支持纹理旋转。
* **文件柜对象** 仅允许在3D晕影中使用。 它们用于编写具有复杂布局要求的厨房和浴室橱柜。 文件柜对象接受可重复的纹理并特别创作 *封包样式文件* 包含可调整大小的机柜面板图像。

除了基本对象类型之外，还支持两种特殊的重叠对象：

* **静态重叠对象** 是不接受材料的对象。 2D和3D晕影均允许使用。 它们可用于房间场景中的可移动附件、可渲染重叠对象后的投影，以及类似应用程序。
* **窗饰框架对象** 提供用于应用窗口覆盖样式文件的放置信息，这些文件独立于晕影进行创作，并可在晕影之间共享。

对象被收集到 *对象组*，类似于文件系统。 分组通常基于它们代表的物理对象的结构（例如“所有文件柜”组可能包含“基本文件柜”和“壁文件柜”）。 允许任意数量的组级别。 分组支持将材料应用于多个类似对象。

* [场景坐标](c-ir-scene-coordinates.md)
* [材质分辨率](c-ir-material-resolution.md)
