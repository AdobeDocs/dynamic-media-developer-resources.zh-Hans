---
description: 将资产上传到Scene7 Production System涉及一个或多个HTTP POST请求，这些请求设置一个作业以协调与已上传文件关联的所有日志活动。
seo-description: 将资产上传到Scene7 Production System涉及一个或多个HTTP POST请求，这些请求设置一个作业以协调与已上传文件关联的所有日志活动。
seo-title: 通过HTTP POST将资产上传到UploadFile Servlet
solution: Experience Manager
title: 通过HTTP POST将资产上传到UploadFile Servlet
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4

---


# 通过HTTP POST将资产上传到UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

将资产上传到Scene7 Production System涉及一个或多个HTTP POST请求，这些请求设置一个作业以协调与已上传文件关联的所有日志活动。

使用以下URL访问UploadFile Servlet:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>上传作业的所有POST请求都必须源于相同的IP地址。

**访问Scene7区域的URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理位置 </p> </th> 
   <th colname="col2" class="entry"> <p>生产URL </p> </th> 
   <th colname="col3" class="entry"> <p>暂存URL（用于预生产开发和测试） </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>北美 </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>欧洲、中东、亚洲 </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本／亚太地区 </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## 上传作业的工作流 {#section-873625b9512f477c992f5cdd77267094}

上传作业由一个或多个HTTP POST组成，这些HTTP POST使用通 `jobHandle` 用方式将处理关联到同一作业中。 每个请求都 `multipart/form-data` 经过编码，由以下表单部分组成：

>[!NOTE]
>
>上传作业的所有POST请求都必须源于相同的IP地址。

| HTTP POST表单部分|说明||-|-||`auth`|必需。 指定身份验证和客户端信息的XML authHeader文档。 请参 **阅SOAP下的** “请求 [身份验证](/help/aem-ips-api/c-wsdl-versions.md)”。 |
|`file params` |  可选. 您可以包含一个或多个要随每个POST请求一起上传的文件。 每个文件部分都可以在Content-Disposition头中包含一个文件名参数，如果未指定任何参数，则该参数将用作IPS中的目标 `uploadPostParams/fileName` 文件名。 |

| HTTP POST表单部分| uploadPostParams元素名称|类型|说明||-|-|-|-||`uploadParams` (必需。 指定上 `uploadParams` 传参数的XML文档)| `companyHandle`|`xsd:string`|必需。 处理要将文件上传到的公司。 |
|`uploadParams` (必需. 指定上 `uploadParams` 传参数的XML文档)|`jobName`|`xsd:string`| `jobName` |需要或 `jobHandle` 必需。 上传作业的名称。 |
|`uploadParams` (必需. 指定上 `uploadParams` 传参数的XML文档)|`jobHandle`|`xsd:string`| `jobName` |需要或 `jobHandle` 必需。 处理在上一个请求中启动的上传作业。 |
|`uploadParams` (必需. 指定上 `uploadParams` 传参数的XML文档)|`locale`|`xsd:string`|可选。 本地化语言和国家代码。 |
|`uploadParams` (必需. 指定上 `uploadParams` 传参数的XML文档)|`description`|`xsd:string`|可选。 作业的说明。 |
|`uploadParams` (必需. 指定上 `uploadParams` 传参数的XML文档)|`destFolder`|`xsd:string`|可选。 目标文件夹路径以作为文件名属性前缀，尤其是对于浏览器和其他可能不支持文件名完整路径的客户端。 |
|`uploadParams` (必需. 指定上 `uploadParams` 传参数的XML文档)|`fileName`|`xsd:string`|可选。 目标文件的名称。 覆盖filename属性。 |
|`uploadParams` (必需. 指定上 `uploadParams` 传参数的XML文档)|`endJob`|`xsd:boolean`|可选。 默认值为 false。|
|`uploadParams` (必需. 指定上 `uploadParams` 传参数的XML文档)|`uploadParams`|`types:UploadPostJob`|如果这是现有活动作业的后续请求，则为可选。 如果存在现有作业，则忽 `uploadParams` 略该作业，并使用现有的作业上传参数。 请参 [阅UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

块内有 `<uploadPostParams>` 指定所包 `<uploadParams>` 含文件处理的块。

请参 [阅UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)。

虽然您可能认为，作 `uploadParams` 为同一作业的一部分，单个文件的参数可以更改，但情况并非如此。 对整个作 `uploadParams` 业使用相同的参数。

对新上传作业的初始POST请求应指定该参数，优选地，使用唯一作业名来简化后续作业状态轮询和作业日志查询。 `jobName` 对同一上传作业的其他POST请求应使用从 `jobHandle` 初始请求返回的 `jobName`值指定 `jobHandle` 该参数而不是参数。

上传作业的最终POST请求应将该参 `endJob` 数设置为true，以便此作业不会对将来的文件进行POST。 而这又允许在收录所有POST文件后立即完成作业。 否则，如果在30分钟内未收到任何其他POST请求，则作业将超时。

## UploadPOST响应 {#section-421df5cc04d44e23a464059aad86d64e}

对于成功的POST请求，响应体将是XML `uploadPostReturn` 文档，如XSD在以下内容中所指定：

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

返回 `jobHandle` 的内容会传递到同一作 `uploadPostParams`业的任何后 `jobHandle` 续POST请求的／参数中。 您还可以使用它对工序的作业状态进行 `getActiveJobs` 轮询，或将作业日志与工序查询 `getJobLogDetails` 。

如果处理POST请求时出错，则响应主体由Faults中所述的API故障类型之一组 [成](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)。

## POST请求示例 {#section-810fe32abdb9426ba0fea488dffadd1e}

```
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## POST响应示例——成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## POST响应示例——错误 {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

