---
title: 使用Responsive图像库
description: 要将响应式图像库添加到网页并使用库管理现有图像，请完成以下步骤。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# 使用Responsive图像库{#using-responsive-image-library}

要将响应式图像库添加到网页并使用库管理现有图像，请完成以下步骤。

**使用响应图像库**

1. 在Dynamic Media Classic中，[创建图像预设](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing)，以防您计划将Responsive图像库与预设一起使用。

   定义与响应图像库一起使用的图像预设时，请勿使用任何影响图像大小的设置，如`wid=`、`hei=`或`scl=`。 请勿在图像预设中指定任何大小字段。 相反，请将其保留为空白值。
1. 将库JavaScript文件添加到您的网页。

   在使用库API之前，请确保包含`responsive_image.js`。 此JavaScript文件位于标准IS-Viewers部署的`libs/`子文件夹中：

   `<s7viewers_root>/libs/responsive_image.js`
1. 设置现有图像。

   库会从其正在处理的图像实例中读取某些配置属性。 在为此类图像调用`s7responsiveImage` API函数之前定义属性。

   还建议您将现有图像URL放入`data-src`属性中。 然后，将现有`src`属性设置为将一个1x1 GIF图像编码为数据URI。 这样可以减少网页在加载时发送的HTTP请求数。 但请注意，如果需要SEO（搜索引擎优化），最好在图像实例上设置`title`属性。

<!--
   The following is an example of defining `data-breakpoints` attribute for the image and using a 1x1 GIF encoded as Data URI:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```
-->

1. 为库管理的每个图像实例调用`s7responsiveImage` API函数。

   为库管理的每个图像实例调用`s7responsiveImage` API函数。 进行此类调用后，库会根据网页布局中`IMG`元素的运行时大小和设备屏幕的密度，使用从图像服务下载的图像替换原始图像。

   以下代码是对图像调用`s7responsiveImage` API函数的示例，假定`responsiveImage`是该图像的ID：

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 示例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

库支持同时处理网页上的多个图像实例。 因此，请对您希望库管理的每个图像重复上述步骤1和2。

网页负责设置图像元素的样式，使其在大小上更加灵活。 Responsive图像库本身不区分固定大小图像和“流畅”图像。 如果应用于固定大小的图像，则只加载新图像一次。

<!--
The following code is a complete example of a trivial web page that has a single fluid image managed by the Responsive Image library. The example contains extra CSS styling to make the image "responsive" to the web browser window size:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>

```
-->

**使用智能裁切**

AEM 6.4和Dynamic Media Viewer 5.9中有两种智能裁剪模式可用：

* **手动** — 用户定义的断点和相应的图像服务命令在图像元素的属性中定义。
* **智能裁切** — 将自动从投放服务器中检索计算智能裁切再现。 使用图像元素的运行时大小选择最佳演绎版。

要使用智能裁剪模式，请将`data-mode`属性设置为`smart crop`。 例如：

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

当断点更改时，关联的图像元素在运行时调度`s7responsiveViewer`事件。

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
