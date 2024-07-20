---
description: 响应式图像库是一个JavaScript模块，可动态调整从Dynamic Media提供并嵌入响应式网页中的图像质量。 此外，它还在具有高密度屏幕的设备上提供改进的图像质量。 库还可以响应地呈现来自智能裁切和智能色板的结果。
solution: Experience Manager
title: 关于响应图像库
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# 关于响应图像库{#about-responsive-image-library}

响应式图像库是一个JavaScript模块，可动态调整从Dynamic Media提供并嵌入响应式网页中的图像质量。 此外，它还在具有高密度屏幕的设备上提供改进的图像质量。 库还可以响应地呈现来自智能裁切和智能色板的结果。

## 演示URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

响应图像库的最简单用例是定义图像宽度的断点值列表。 此列表确保在因用户调整浏览器窗口大小或更改设备方向而更改网页布局而导致图像大小调整时加载和显示相应的演绎版。 库会持续监控屏幕上的图像大小，每当达到新的断点宽度时，它都会从Dynamic Media中获取新的图像演绎版。

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
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>下面是一个简单示例，其中响应式图像位于占网页宽度50%的容器中。 每次调整浏览器窗口大小时，容器宽度都会更改。 当图像宽度达到所配置的断点之一（该断点被设置为200、400、600和800像素用于说明目的）时，将下载并显示新的演绎版。 目的是避免加载不必要的超大图像，并节省网络带宽。 </p> <p>单击URL以打开网页、调整浏览器窗口大小并监视网络流量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>以下Bootstrap示例展示了网页中的相同用例。 根据BootstrapCSS，向其中添加响应图像的布局单元格可以采用以下宽度之一：360、720和940像素。 这些值就是作为断点传递到Responsive图像库的值。 因此，Dynamic Media可确保有效使用客户端的网络带宽。 此外，它还可确保按照当前网页布局所需的确切大小显示图像，而不会因缩放客户端浏览器而出现任何视觉伪像。 </p> <p>单击URL以打开网页，调整浏览器窗口大小以点击不同的布局断点，并监控网络流量。 </p> <p>更高级的用例包括将不同的图像预设和/或图像服务命令与不同的断点值相关联。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>在下例中，使用了不同图像质量和不同断点大小格式的图像预设。 对于小的断点，应用了低质量预设，这会强制图像服务将压缩为仅六种颜色的GIF图像返回。 中断点正在使用为高压缩JPEG配置的图像预设。 最大断点与使用无损PNG的高质量图像预设相关联。 基于具有较大屏幕的设备具有较大的带宽和处理能力的假设，这种方法确保高质量图像被传送到这样的设备。 </p> <p>单击URL以打开网页，将Web浏览器窗口的大小从大调整为小，并注意图像质量下降的方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>除了图像预设之外，还可以将特定的图像服务命令与断点相关联。 以下示例显示了如何在屏幕图像大小变小时逐渐将横幅图像裁切到感兴趣区域。 在此，最大的断点根本没有任何图像提供命令，因此横幅图像完全可见。 在中断点处应用温和裁剪，使只有文本为“正在运行”的流道可见。 在小断点时，应用更多的裁切，以便只显示产品。 </p> <p>单击URL以打开网页并调整浏览器窗口大小。 请注意图像是如何逐渐裁剪的，从大尺寸裁剪到小尺寸。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>您还可以结合使用图像服务命令和图像服务模板来根据图像大小控制某些模板参数。 在下个示例中，使用了图像服务模板，其中文本叠加的字体大小是使用<span class="codeph"> $fontsize </span>参数参数化的。 响应式图像配置为对较小的图像使用较大的字体大小，以确保文本始终可读： </p> </td> 
  </tr> 
 </tbody> 
</table>

## 系统要求 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**服务器硬件和软件**

* Dynamic Media图像服务6.0.1或更高版本。

**客户端浏览器最低要求**

* Microsoft® Windows® 7或更高版本；macOS X 10.8或更高版本。
* Firefox 23、Safari 6、Chrome 29、IE 9或更高版本。
* iOS 6或更高版本。
* 已在iPhone3GS或更高版本以及iPad2或更高版本上获得认证（仅限本机浏览器）。
* Android™ OS 2.3或更高版本。
* 当前不支持移动设备上的Internet Explorer。
