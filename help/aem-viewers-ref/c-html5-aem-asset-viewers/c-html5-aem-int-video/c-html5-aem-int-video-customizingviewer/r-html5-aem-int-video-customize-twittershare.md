---
description: Twitter共享工具由添加到“社交共享”面板的按钮组成。 单击按钮时，用户将被重定向到由社交服务提供的共享对话框。 按钮的位置完全由社交共享工具管理。
solution: Experience Manager
title: Twitter分享
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Twitter共享{#twitter-share}

Twitter共享工具由添加到“社交共享”面板的按钮组成。 单击按钮时，用户将被重定向到由社交服务提供的共享对话框。 按钮的位置完全由社交共享工具管理。

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Twitter共享按钮的外观由以下CSS类选择器控制：

```
.s7interactivevideoviewer .s7twittershare
```

**Twitter共享工具的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同外观应用于不同的按钮状态。

通过设置Social共享面板的CSS类上的`display:none` CSS属性，可以从该面板中删除该按钮。

按钮工具提示可以本地化。 请参阅[用户界面元素本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

## 示例 {#section-5a8837ea208e48ed8dfa6a3c1a514492}

要设置28 x 28像素的Twitter共享按钮，并针对四个不同的按钮状态中的每一个显示不同的图像：

```
.s7interactivevideoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```

