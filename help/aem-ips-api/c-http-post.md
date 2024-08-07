---
title: 通过HTTP POST将资产上传到UploadFile Servlet
description: 将资源上传到 [!DNL Dynamic Media] Classic中涉及一个或多个HTTPPOST请求，这些请求设置作业以协调与上传的文件关联的所有日志活动。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# 通过HTTP POST将资产上传到UploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

将资源上传到Dynamic Media Classic涉及一个或多个HTTPPOST请求，这些请求设置作业以协调与上传文件关联的所有日志活动。

使用以下URL访问UploadFile Servlet：

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>上载作业的所有POST请求必须来自相同的IP地址。

**访问Dynamic Media地区的URL**

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
   <td colname="col1"> <p>日本/亚太 </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## 上载作业的工作流 {#section-873625b9512f477c992f5cdd77267094}

上载作业包含一个或多个HTTP POST，这些HTTP POST使用公共`jobHandle`将处理关联到同一作业。 每个请求都经过`multipart/form-data`编码，由以下表单部分组成：

>[!NOTE]
>
>上载作业的所有POST请求必须来自相同的IP地址。

|  HTTPPOST表单部件  |  描述  |
|---|---|
| `auth`  |   必需。 指定身份验证和客户端信息的XML authHeader文档。 请参阅[SOAP](/help/aem-ips-api/c-wsdl-versions.md)下的&#x200B;**请求身份验证**。 |
| `file params`  |   可选。 您可以包含一个或多个要随每个POST请求上传的文件。 每个文件部分都可在Content-Disposition标头中包含一个文件名参数，如果未指定`uploadPostParams/fileName`参数，则该参数将用作IPS中的目标文件名。 |

|  HTTPPOST表单部件   |  uploadPostParams元素名称   |  类型   |  描述   |
|---|---|---|---|
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档   |   `companyHandle`  |  `xsd:string`  | 必需。 将文件上传到的公司的句柄。  |
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档 | `jobName`  |  `xsd:string`  | 需要`jobName`或`jobHandle`。 上载作业的名称。  |
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档 | `jobHandle`  |  `xsd:string`  | 需要`jobName`或`jobHandle`。 对在上一个请求中启动的上载作业的处理。  |
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档 | `locale`  |  `xsd:string`  | 可选。 本地化的语言和国家/地区代码。  |
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档 | `description`  |  `xsd:string`  | 可选。 作业的描述。  |
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档 | `destFolder`  |  `xsd:string`  | 可选。 文件名属性的前缀的目标文件夹路径，特别是对于可能不支持文件名中完整路径的浏览器和其他客户端。  |
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档 | `fileName`  |  `xsd:string`  | 可选。 目标文件的名称。 覆盖filename属性。 |
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档 | `endJob`  |  `xsd:boolean`  | 可选。 默认值为 false。 |
| `uploadParams` (必需。 指定上载参数的XML `uploadParams`文档 | `uploadParams`  |  `types:UploadPostJob`  | 如果这是针对现有活动作业的后续请求，则为可选。 如果存在现有作业，则忽略`uploadParams`并使用现有作业上载参数。 查看[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

`<uploadPostParams>`块内是指定处理所包含文件的`<uploadParams>`块。

查看[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)。

虽然您可能认为可以将各个文件的`uploadParams`参数作为同一作业的一部分进行更改，但情况并非如此。 对整个作业使用相同的`uploadParams`参数。

新上载作业的初始POST请求应指定`jobName`参数，最好使用唯一的作业名称来简化后续作业状态轮询和作业日志查询。 对于同一上载作业的其他POST请求，应使用从初始请求返回的`jobHandle`值指定`jobHandle`参数而不是`jobName`。

上载作业的最终POST请求应将`endJob`参数设置为true，以便将来不会为此作业发布任何文件。 反过来，这允许作业在摄取所有POSTed文件后立即完成。 否则，如果未在30分钟内收到其他POST请求，作业将超时。

## uploadpost响应 {#section-421df5cc04d44e23a464059aad86d64e}

对于成功的POST请求，响应正文是XML `uploadPostReturn`文档，如XSD在以下内容中所指定：

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

对于同一作业的任何后续POST请求，返回的`jobHandle`在`uploadPostParams`/`jobHandle`参数中传递。 您还可以使用它来轮询`getActiveJobs`操作的作业状态，或查询`getJobLogDetails`操作的作业日志。

如果处理POST请求时出错，则响应正文将由[故障](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)中所述的API故障类型之一组成。

## 示例POST请求 {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
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

## 示例POST响应 — 成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## 示例POST响应 — 错误 {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
