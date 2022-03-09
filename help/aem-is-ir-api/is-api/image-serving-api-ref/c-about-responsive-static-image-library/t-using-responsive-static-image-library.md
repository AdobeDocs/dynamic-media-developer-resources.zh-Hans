---
title: 使用响应式图像库
description: 要向网页添加响应式图像库并使用库管理现有图像，请完成以下步骤。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# 使用响应式图像库{#using-responsive-image-library}

要向网页添加响应式图像库并使用库管理现有图像，请完成以下步骤。

**使用响应式图像库**

1. 在Dynamic Media Classic, [创建图像预设](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) 以防您计划将响应式图像库与预设结合使用。

   在定义与响应式图像库一起使用的图像预设时，请勿使用任何影响图像大小的设置，例如 `wid=`, `hei=`或 `scl=`. 请勿在图像预设中指定任何大小字段。 而是将它们保留为空值。
1. 将库JavaScript文件添加到您的网页中。

   在使用库API之前，请确保在 `responsive_image.js`. 此JavaScript文件位于 `libs/` 标准IS — 查看器部署的子文件夹：

   `<s7viewers_root>/libs/responsive_image.js`
1. 设置现有图像。

   库会从它正在使用的图像实例中读取特定配置属性。 在 `s7responsiveImage` 为此类图像调用API函数。

   还建议您将现有的图像URL放入 `data-src` 属性。 然后，设置现有 `src` 属性，以将1x1GIF图像编码为数据URI。 这样，可减少网页在加载时发送的HTTP请求数。 但请注意，如果需要SEO（搜索引擎优化），则最好设置 `title` 属性。

   以下是定义 `data-breakpoints` 属性，并使用编码为数据URI的1x1GIF:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. 调用 `s7responsiveImage` 库管理的每个图像实例的API函数。

   调用 `s7responsiveImage` 库管理的每个图像实例的API函数。 在进行此类调用后，库会根据 `IMG` 元素，以及设备屏幕的密度。

   以下代码是调用的示例 `s7responsiveImage` API在图像上运行，假定 `responsiveImage` 是该图像的ID:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 示例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

库支持同时处理网页上的多个图像实例。 因此，请对您希望库管理的每个图像重复上述步骤1和2。

网页负责设置图像元素的样式，以使其在大小上更加灵活。 响应式图像库本身不会区分固定大小和“流体”图像。 如果应用于固定大小的图像，则只加载一次新图像。

以下代码是一个简单网页的完整示例，该网页具有由响应式图像库管理的单个流体图像。 该示例包含额外的CSS样式，以使图像对Web浏览器窗口大小“响应”：

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

**使用智能裁剪**

AEM 6.4和Dynamic Media查看器5.9中提供了两种智能裁剪模式：

* **手动**  — 在图像元素的属性中定义用户定义的断点和相应的图像服务命令。
* **智能裁剪**  — 从投放服务器自动检索计算的智能裁剪呈现版本。 使用图像元素的运行时大小选择最佳演绎版。

要使用智能裁剪模式，请设置 `data-mode` 属性 `smart crop`. 例如：

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

关联的图像元素调度 `s7responsiveViewer` 断点更改时的事件。

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
