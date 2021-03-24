---
description: 自定义视频查看器
keywords: 响应
solution: Experience Manager
title: 自定义视频查看器
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 0%

---


# 自定义视频查看器{#customizing-video-viewer}

通过创建自定义CSS，可以完成所有可视自定义和大多数行为自定义。

建议的工作流程是为相应的查看器使用默认的CSS文件，将其复制到其他位置，对其进行自定义，并在`style=`命令中指定自定义文件的位置。

默认CSS文件位于以下位置：

`<s7_viewers_root>/html5/VideoViewer.css`

自定义CSS文件必须包含与默认类声明相同的类声明。 如果省略类声明，则查看器无法正常工作，因为它不为用户界面元素提供内置默认样式。

提供自定义CSS规则的另一种方法是直接在网页或链接的外部CSS规则之一中使用嵌入样式。

创建自定义CSS时，请记住，查看器将`.s7videoviewer`类分配给其容器DOM元素。 如果使用随`style=`命令传递的外部CSS文件，请将`.s7videoviewer`类用作CSS规则的子代选择器中的父类。 如果在网页上嵌入样式，则还可以通过以下容器DOM元素的ID来限定此选择器：

`#<containerId>.s7videoviewer`

## 构建响应式设计的CSS {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

可以在CSS中目标不同的设备，使内容显示方式根据用户的设备而有所不同。 此定位包括但不限于不同的用户界面元素大小和图稿分辨率。

查看器支持两种创建响应式设计的CSS的机制：CSS标记和标准CSS媒体查询。 您可以单独或一起使用这些组件。

**CSS标记**

为了帮助创建响应式设计的CSS，查看器支持CSS标记，这些特殊CSS类基于运行时查看器大小和当前设备上使用的输入类型动态分配给顶级查看器容器元素。

第一组CSS标记包括`.s7size_large`、`.s7size_medium`和`.s7size_small`类。 它们会根据查看器容器的运行时区域进行应用。 即，如果查看器区域等于或大于通用桌面监视器`.s7size_large`的大小；如果区域大小与通用平板电脑设备`.s7size_medium`相近，则分配该区域。 对于类似于手机屏幕的区域设置`.s7size_small`。 这些CSS标记的主要用途是为不同的屏幕和查看器大小创建不同的用户界面布局。

第二组CSS标记包括`.s7mouseinput`和`.s7touchinput`。 `.s7touchinput` is set if current device has touch input capabilities;否则， `.s7mouseinput` 将使用。这些标记旨在为不同的输入类型创建具有不同屏幕大小的用户界面输入元素，因为通常触摸输入需要较大的元素。 如果设备同时具有鼠标输入和触摸功能，则设置`.s7touchinput`，并且查看器呈现适合触摸的用户界面。

以下范例CSS将带鼠标输入的系统上的播放/暂停按钮大小设置为28 x 28像素，将触控设备上的56 x 56像素。 此外，如果查看器尺寸变得很小，它会完全隐藏按钮：

```
.s7videoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7videoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7videoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

要目标像素密度不同的设备，请使用CSS媒体查询。 以下媒体查询块将包含特定于高密度屏幕的CSS:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

使用CSS标记是构建响应式设计的CSS的最灵活方式，因为它不仅允许您目标设备屏幕大小，还允许显示实际的查看器大小，这对于响应式设计页面布局非常有用。

将默认查看器CSS文件用作CSS标记方法的示例。

**CSS媒体查询**

设备传感也可以使用纯CSS媒体查询完成。 仅当在相应设备上运行给定媒体查询块时，才应用它中包含的所有内容。

应用到移动查看器时，请按以下列顺序在CSS中定义四个CSS媒体查询:

1. 仅包含所有触控设备的特定规则。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. 仅包含针对具有高分辨率屏幕的平板电脑的特定规则。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. 仅包含所有移动电话的特定规则。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 仅包含针对具有高分辨率屏幕的移动电话的特定规则。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

使用CSS媒体查询方法，您应按照如下方式通过设备传感组织CSS:

* 首先，特定于桌面的部分定义所有属性，这些属性是特定于桌面的，或是所有屏幕通用的。
* 其次，四个媒体查询应按上面定义的顺序排列，并提供特定于相应设备类型的CSS规则。

无需在每个媒体查询中重复整个查看器CSS。 只有特定于给定设备的属性在媒体查询中重新定义。

## CSS Sprite {#section-9b6d8d601cb441d08214dada7bb4eddc}

许多查看器用户界面元素使用位图图稿设置样式，并具有多个不同的可视状态。 一个不错的示例是按钮，它通常至少具有3种不同的状态：“up”、“over”和“down”。 每个状态都需要分配自己的位图图稿。

使用经典的样式方法，CSS将针对用户界面元素的每个状态对服务器上的单个图像文件单独引用。 以下是用于设置全屏按钮样式的示例CSS:

```
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

此方法的缺点是，当元素第一次与之交互时，终端用户体验到闪烁或延迟的用户界面响应。 此操作之所以发生，是因为尚未下载新元素状态的图像图稿。 此外，由于对服务器的HTTP调用数量增加，此方法可能会对性能产生轻微的负面影响。

CSS Sprite是一种不同的方法，将所有元素状态的图像图稿组合到一个称为“Sprite”的PNG文件中。 此类“Sprite”具有给定元素的所有可视状态，这些元素会依次放置。 当用Sprite设置用户界面元素的样式时，CSS中的所有不同状态都引用了相同的Sprite图像。 此外，每个状态都使用`background-position`属性来指定使用“sprite”图像的哪一部分。 您可以以任何合适的方式构建“Sprite”图像。 查看器通常垂直堆叠。 下面是一个基于“sprite”的示例，从上面设置同一个全屏按钮的样式：

```
.s7videoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## 一般样式说明和建议{#section-097418bd618740bba36352629e4d88e1}

* CSS中指向外部资源的所有路径都会针对CSS位置而不是查看器HTML页面的位置进行解析。 将默认CSS复制到其他位置时，请记住考虑此规则。 在自定义CSS中复制默认资源或更新路径。
* 位图图稿的首选格式为PNG。
* 位图图稿使用`background-image`属性分配给用户界面元素。
* 用户界面元素的`width`和`height`属性定义其逻辑大小。 传递给`background-image`的位图的大小不影响逻辑大小。

* 要使用Retina等高分辨率屏幕的高像素密度，请指定比逻辑用户界面元素大两倍的位图图稿。 然后，应用`-webkit-background-size:contain`属性，将背景缩小到逻辑用户界面元素大小。
* 要从用户界面中删除按钮，请将`display:none`添加到其CSS类。
* 您可以对CSS支持的颜色值使用各种格式。 如果需要透明度，请使用格式`rgba(R,G,B,A)`。 否则，可以使用格式`#RRGGBB`。

* 使用CSS自定义查看器用户界面时，不支持对查看器元素设置样式。 `!IMPORTANT`尤其不应使用`!IMPORTANT`规则覆盖查看器或查看器SDK提供的任何默认或运行时样式。 其原因在于，它可能会影响正确组件的行为。 相反，您应使用具有适当特异性的CSS选择器来设置本参考指南中介绍的CSS属性。

## 常用用户界面元素{#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下是适用于视频查看器的用户界面元素引用文档：
