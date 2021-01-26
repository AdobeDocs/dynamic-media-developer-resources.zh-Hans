---
description: 响应式图像库是一个JavaScript模块，可动态调整从Dynamic Media提供并嵌入到响应式网页中的图像质量。 此外，它在具有高密度屏幕的设备上提供改进的图像质量。 库还可以响应式渲染“智能裁剪”和“智能色板”的结果。
solution: Experience Manager
title: 关于响应式图像库
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 0%

---


# 关于响应式图像库{#about-responsive-image-library}

响应式图像库是一个JavaScript模块，可动态调整从Dynamic Media提供并嵌入到响应式网页中的图像质量。 此外，它在具有高密度屏幕的设备上提供改进的图像质量。 库还可以响应式渲染“智能裁剪”和“智能色板”的结果。

## 演示URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

响应式图像库最简单的用例是为图像宽度定义断点值的列表。 此列表可确保在调整图像大小时加载和显示相应的再现，因为用户在调整浏览器窗口大小或更改设备方向时，网页布局会发生变化。 库会持续监视屏幕图像大小，每次达到新的断点宽度时，它都会从Dynamic Media获取新的图像再现。

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>演示URL </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>以下是响应式图像位于占网页宽度50%的容器内的一个简单示例。 每次调整容器窗口大小时，浏览器宽度都会发生变化。 当图像宽度达到某个已配置断点时（为说明目的而设置为200、400、600和800像素），将下载并显示新的再现。 其目标是避免加载不必要的大图像，并节省网络带宽。 </p> <p>单击该URL以打开网页、调整浏览器窗口大小和监视网络流量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>以下Bootstrap示例说明了网页中的相同用例。 根据BootstrapCSS，将响应式图像添加到的布局单元格可以采用以下宽度之一：360、720和940像素。 这些值是作为断点传递到响应式图像库的确切值。 因此，Dynamic Media确保客户端的网络带宽得到有效利用。 此外，它还确保图像以给定当前网页布局所需的完全大小显示，而不会因缩放客户端浏览器而产生任何视觉伪像。 </p> <p>单击URL以打开网页，调整浏览器窗口大小以达到不同的布局断点，并监视网络流量。 </p> <p>更高级的用例包括将不同的图像预设或图像服务命令（或两者）与不同的断点值相关联。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>在下一个示例中，将使用不同图像质量和格式的图像预设来适应不同的断点大小。 对于小的断点，会应用低质量预设，强制图像服务返回仅压缩为六色的GIF图像。 中断点正在使用为高压缩JPEG配置的图像预设。 最大的断点与使用无损PNG的高质量图像预设相关联。 这种方法基于具有较大屏幕的设备具有更大的带宽和处理能力的假设，确保高质量图像被传送到这种设备。 </p> <p>单击该URL以打开网页，将Web浏览器窗口从大调整为小，并注意图像质量的降低。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>除了图像预设之外，还可以将特定图像服务命令与断点相关联。 以下示例显示了当屏幕图像大小变小时，如何将横幅图像逐渐裁剪到感兴趣区域。 此处，最大的断点根本没有任何图像服务命令，因此横幅图像完全可见。 在中断点应用中度裁剪，使得只有文本为“正在运行”的运行器可见。 在小断点处，将应用更多裁剪，以便只显示产品。 </p> <p>单击该URL以打开网页并调整浏览器窗口的大小。 注意图像在您从较大到较小时会逐渐裁切。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>您还可以将图像服务命令与图像服务模板结合使用，以根据图像大小控制某些模板参数。 在下一个示例中，使用图像服务模板，其中使用<span class="codeph"> $fontsize </span>参数参数化文本叠加的字体大小。 响应式图像配置为对较小的图像使用较大的字体大小，以确保文本始终可读： </p> </td> 
  </tr> 
 </tbody> 
</table>

## 系统要求 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**服务器硬件和软件**

* Dynamic Media图像服务6.0.1或更高版本。

**客户端浏览器最低要求**

* Microsoft® Windows® 7或更高版本；Mac OS X 10.8或更高版本。
* Firefox 23、Safari 6、Chrome 29、IE 9或更高版本。
* iOS 6或更高版本。
* 已在iPhone3GS或更高版本以及iPad2或更高版本（仅限本机浏览器）上认证。
* Android OS 2.3或更高版本。
* 目前不支持移动设备上的Internet Explorer。

