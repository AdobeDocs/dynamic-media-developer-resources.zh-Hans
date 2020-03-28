---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.iscommand
solution: Experience Manager
title: FlyoutZoomView.iscommand
topic: Dynamic media
uuid: 1b776481-c40b-4892-9891-ebf3e713a4dc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> </p> <p>应用于FlyoutZoomView主图像和放大视图的图像服务命令字符串。 如果在URL中指定了该属性，请确保将&amp;和 <span class="codeph"> =</span> ( <span class="codeph"> &amp;26</span> )的所有匹配项 <span class="codeph"> （分别编码为%3D）</span><span class="codeph"></span>和%3D。 </p> <p> <p>注意： 不支持图像大小调整操作命令。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 属性 {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

可选。

## 默认 {#section-a08032f0fcf041c09e63c0238a339fc9}

无。

## 示例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

当在查看器URL中指定时：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

在配置数据中指定时：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
