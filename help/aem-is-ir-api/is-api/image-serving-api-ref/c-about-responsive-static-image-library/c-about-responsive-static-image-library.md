---
description: 响应式图像库是一个JavaScript模块，可动态调整从Dynamic Media提供并嵌入到响应式网页中的图像质量。 此外，它在具有高密度屏幕的设备上提供了改进的图像质量。 库还可以响应性地渲染来自智能裁剪和智能色板的结果。
solution: Experience Manager
title: 关于响应式图像库
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 417fd2540c15762356dfb60aa7eb635ee5f74d13
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# 关于响应式图像库{#about-responsive-image-library}

响应式图像库是一个JavaScript模块，可动态调整从Dynamic Media提供并嵌入到响应式网页中的图像质量。 此外，它在具有高密度屏幕的设备上提供了改进的图像质量。 库还可以响应性地渲染来自智能裁剪和智能色板的结果。

## 演示URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

响应式图像库的最简单用例是，为图像宽度定义断点值列表。 此列表可确保在调整图像大小时加载并显示相应的呈现版本，因为用户调整浏览器窗口大小或更改设备方向时，网页布局会发生更改。 库会持续监控屏幕上的图像大小，每当达到新的断点宽度时，它都会从Dynamic Media中获取新的图像呈现版本。

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
   <td colname="col2"> <p>以下是一个简单的示例，其中响应式图像位于占网页宽度50%的容器内。 每次调整浏览器窗口的大小时，容器宽度都会发生更改。 当图像宽度达到某个已配置断点（为说明目的而设置为200、400、600和800像素）时，将下载并显示新的呈现版本。 其目标是避免加载不必要的大图像，并节省网络带宽。 </p> <p>单击URL以打开网页、调整浏览器窗口大小并监视网络流量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>以下Bootstrap示例说明了网页中的相同用例。 根据BootstrapCSS，将响应式图像添加到的布局单元格可以采用以下宽度之一：360、720和940像素。 这些值正是作为断点传递到响应式图像库的内容。 因此，Dynamic Media可确保有效地使用客户端的网络带宽。 此外，它还可确保以给定当前网页布局所需的确切大小显示图像，而无需缩放客户端浏览器时出现任何可视工件。 </p> <p>单击URL可打开网页、调整浏览器窗口大小以达到不同的布局断点并监控网络流量。 </p> <p>更高级的用例包括将不同的“图像预设”或“图像提供”命令（或同时将这两个命令）与不同的断点值关联。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>在下一个示例中，会针对不同的断点大小使用不同图像质量和格式的图像预设。 对于较小的断点，会应用低质量的预设，这会强制图像服务返回仅压缩为六色的GIF图像。 媒体断点使用的是为JPEG配置的高压缩图像预设。 最大断点与使用无损PNG的高质量图像预设相关联。 这种方法基于具有较大屏幕的设备具有更大带宽和处理能力的假设，确保将高质量图像传送到这种设备。 </p> <p>单击该URL可打开网页，将Web浏览器窗口的大小从大到小调整，并注意图像质量如何降低。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>除了图像预设之外，还可以将特定的图像提供命令与断点相关联。 以下示例显示了在屏幕图像大小变小时，如何能够将横幅图像逐渐裁剪到感兴趣的区域。 在此，最大的断点根本没有任何“图像提供”命令，因此横幅图像是完全可见的。 在中断点处应用中度裁剪，从而仅使文本为“正在运行”的运行器可见。 在较小的断点处，会应用更多裁剪以便仅显示产品。 </p> <p>单击URL以打开网页并调整浏览器窗口的大小。 请注意图像在从大到小的过程中如何逐渐裁剪。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>您还可以将“图像提供”命令与“图像提供模板”结合使用，以根据图像大小控制某些模板参数。 在下一个示例中，使用了图像提供模板，其中使用<span class="codeph"> $fontsize </span>参数参数化文本叠加的字体大小。 响应式图像配置为使用较大的字体大小来缩小图像大小，以确保文本始终可读： </p> </td> 
  </tr> 
 </tbody> 
</table>

## 系统要求 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**服务器硬件和软件**

* Dynamic Media Image Serving 6.0.1或更高版本。

**客户端浏览器最低要求**

* Microsoft® Windows® 7或更高版本；macOS X 10.8或更高版本。
* Firefox 23、Safari 6、Chrome 29、IE 9或更高版本。
* iOS 6或更高版本。
* 已在iPhone3GS或更高版本以及iPad2或更高版本（仅限本机浏览器）上认证。
* Android™ OS 2.3或更高版本。
* 当前不支持移动设备上的Internet Explorer。
