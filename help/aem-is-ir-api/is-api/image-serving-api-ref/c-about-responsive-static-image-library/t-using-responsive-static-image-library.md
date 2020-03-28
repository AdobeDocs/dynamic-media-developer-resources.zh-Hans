---
description: 要将响应式图像库添加到网页并使用该库管理现有图像，请完成以下步骤。
seo-description: 要将响应式图像库添加到网页并使用该库管理现有图像，请完成以下步骤。
seo-title: 使用响应式图像库
solution: Experience Manager
title: 使用响应式图像库
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# 使用响应式图像库{#using-responsive-image-library}

要将响应式图像库添加到网页并使用该库管理现有图像，请完成以下步骤。

**使用响应式图像库**

1. 在SPS中，创建 [图像预设](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) ，以备您计划将响应式图像库与预设结合使用。

   在定义与响应式图像库一起使用的图像预设时，请勿使用任何影响图像大小的设置， `wid=`如 `hei=`、或 `scl=`。 请勿在图像预设中指定任何大小字段。 相反，将它们保留为空值。
1. 将库JavaScript文件添加到网页。

   在使用库API之前，请确保包含 `responsive_image.js`。 此JavaScript文件位于标准IS- `libs/` Viewers部署的子文件夹中：

   `<s7viewers_root>/libs/responsive_image.js`
1. 设置现有图像。

   库从它使用的图像实例中读取某些配置属性。 在为此类图像调 `s7responsiveImage` 用API函数之前定义属性。

   还建议将现有图像URL放入属 `data-src` 性。 然后，设置现有属 `src` 性，使1x1 GIF图像编码为数据URI。 这样，可减少加载时网页发送的HTTP请求数。 但是，请注意，如果需要SEO（搜索引擎优化），最好在图像实例 `title` 上设置属性。

   以下是为图像定义属 `data-breakpoints` 性并使用编码为数据URI的1x1 GIF的示例：

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 调用库 `s7responsiveImage` 管理的每个图像实例的API函数。

   调用库 `s7responsiveImage` 管理的每个图像实例的API函数。 在这种调用之后，库根据网页布局中元素的运行时大小和设备屏幕密度，将原始图像替换为从图像服务下载的图像。 `IMG`

   以下代码是在图像上调用 `s7responsiveImage` API函数的示例，假定 `responsiveImage` 它是该图像的ID:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 示例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

该库支持同时处理网页上的许多图像实例。 因此，请为希望库管理的每个图像重复上述步骤1和2。

网页有责任设计图像元素的样式，使其变得灵活大小。 响应式图像库本身不区分固定大小和“流体”图像。 如果应用于固定大小的图像，则只加载新图像一次。

以下代码是包含由响应式图像库管理的单个流体图像的次要网页的完整示例。 该示例包含额外的CSS样式，以使图像对Web浏览器窗口大小“响应式”:

```
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

**使用智能裁切**

AEM 6.4和Scene7查看器5.9中提供两种智能裁剪模式：

* **手动** -用户定义的断点和相应的图像服务命令是在图像元素的属性中定义的。
* **智能裁剪** -从投放服务器自动检索计算出的智能裁剪演绎版。 使用图像元素的运行时大小选择最佳再现。

要使用智能裁剪模式，请将属性 `data-mode` 设置为 `smart crop`。 例如：

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

当断点发生更改时，关联的图 `s7responsiveViewer` 像元素会在运行时期间调度事件。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
