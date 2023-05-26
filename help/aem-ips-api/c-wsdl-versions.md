---
description: IPS Web服务受一组WSDL（Web服务描述语言）文档支持，可通过任何安装了IPS Web服务组件的IPS安装访问这些文档。 每个IPS API版本都包含一个引用了版本化目标XML命名空间的新WSDL文件。 还支持以前的WSDL命名空间版本，以便与现有应用程序向后兼容。
solution: Experience Manager
title: IPS Web服务WSDL版本
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 1%

---

# IPS Web服务WSDL版本{#ips-web-service-wsdl-versions}

IPS Web服务受一组WSDL（Web服务描述语言）文档支持，可通过任何安装了IPS Web服务组件的IPS安装访问这些文档。 每个IPS API版本都包含一个引用了版本化目标XML命名空间的新WSDL文件。 还支持以前的WSDL命名空间版本，以便与现有应用程序向后兼容。

## WSDL访问 {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

访问Scene7 WSDL，如下所示。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

的默认值 `<IPS_webapp>` 是 `scene7`.

**服务位置**

服务URL在IPS Web服务WSDL文档的服务部分中指定。 服务URL通常采用以下形式：

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**访问Dynamic Media地区的URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理位置 </p> </th> 
   <th colname="col2" class="entry"> <p>生产URL </p> </th> 
   <th colname="col3" class="entry"> <p>暂存URL（用于生产前的开发和测试） </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>北美 </p> </td> 
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>欧洲、中东、亚洲 </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本/亚太 </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支持的WSDL {#section-ebbba69880f94e9c823f1147974eb404}

请记住，如果要使用最新版本的IPS API中的功能，则可能需要修改代码。 IPS API支持以下版本的WSDL：

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API发行版本 </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API命名空间 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>低于4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

为了使用新功能而需要修改的现有应用程序必须升级到最新的API版本，并且可能需要更改现有代码。 有关详细信息，请参阅更改日志。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**绑定**

IPS API Web服务仅支持SOAP绑定。

**支持的传输**

IPS API SOAP绑定仅支持HTTP传输。 使用HTTPSPOST方法发出所有SOAP请求。

**SOAP操作标头**

要处理请求，请将SOAPAction HTTP标头设置为所请求操作的名称。 WSDL绑定部分中的操作名称属性指定了名称。

**消息格式**

文档/文本样式用于所有具有基于XML架构定义语言( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/))，并在WSDL文件中指定。 所有类型都需要使用WSDL文件中指定的目标命名空间值的限定名称。

**请求身份验证**

在API请求中传递身份验证凭据的首选方法是使用 `authHeader` 元素，如IPS API WSDL中所定义。

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**字段**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 用户 </span> </p> </td> 
   <td colname="col2"> <p> 有效的IPS用户电子邮件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 密码 </span> </p> </td> 
   <td colname="col2"> <p>用户帐户的密码。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> 请求的可选区域设置。 参见 <b>区域设置</b> 了解详细信息。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> 正在调用应用程序名称。 此参数是可选的，但建议将其包含在所有请求中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> 调用应用程序版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> 启用或禁用响应XML的gzip压缩的可选标记。 默认情况下，如果HTTP Accept-Encoding标头指示支持gzip，则响应将进行gzip压缩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> 用于覆盖错误响应的HTTP状态代码的可选参数。 默认情况下，错误响应返回HTTP状态代码500（内部服务器错误）。 某些客户端平台(包括AdobeFlash)无法读取响应正文，除非返回状态代码200 (OK)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此 `authHeader` 元素始终在命名空间中定义 `http://www.scene7.com/IpsApi/xsd`，而不考虑API版本。

以下是使用 `authHeader` 请求SOAP标头中的元素：

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**其他请求身份验证方法**

如果由于某种原因，您的客户端应用程序无法传递 `authHeader` SOAP标头、API请求还可以使用HTTP基本身份验证（如RFC 2617中所指定）指定凭据。

对于HTTP Basic身份验证，每个SOAPPOST请求的HTTP标头部分必须包含格式的标头：

`Authorization: Basic base64(<IPS_user_email>:<password>)`

位置 `base64()` 应用标准Base64编码， `<IPS_user_email>` 是有效IPS用户的电子邮件地址，并且 `<password>` 是用户的密码。

使用初始请求抢先发送授权标头。 如果请求中未包含身份验证凭据， `IpsApiService` 未响应状态代码 `401 (Unauthorized)`. 相反，状态代码为 `500 (Internal Server Error)` 返回一个SOAP错误正文，说明无法对请求进行身份验证。

在IPS 3.8之前，通过SOAP标头实施的身份验证使用 `AuthUser` 和 `AuthPassword` 命名空间中的元素 `http://www.scene7.com/IpsApi`. 例如：

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

此样式仍支持向后兼容性，但已弃用，取而代之的是 `authHeader` 元素。

**请求授权**

在呼叫者的凭证经过验证之后，检查请求以确保呼叫者被授权执行请求的操作。 授权基于呼叫者的用户角色，并且可能还需要检查目标公司、目标用户和其他操作参数。 此外，图像门户用户必须属于具有执行特定文件夹和资产操作所需权限的组。 操作引用部分详细介绍了每个操作的授权要求。

**示例SOAP请求和响应**

以下示例显示完整的 `addCompany` 操作，包括HTTP标头：

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

以及相应的响应：

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**SOAP错误**

当操作遇到异常情况时，将返回SOAP错误作为SOAP消息的主体来代替正常响应。 例如，如果非管理员用户尝试发送以前的 `addCompany` 请求，则会返回以下响应：

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```
