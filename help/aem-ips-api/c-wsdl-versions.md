---
description: IPS Web服務由一組WSDL （Web服務描述語言）檔案支援，可從任何安裝IPS Web服務元件的IPS安裝存取。 每個IPS API版本都包含一個引用了版本化目標XML名稱空間的新WSDL檔案。 也支援舊版WSDL名稱空間，以便與現有應用程式回溯相容。
solution: Experience Manager
title: IPS Web服務WSDL版本
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 1%

---

# IPS Web服務WSDL版本{#ips-web-service-wsdl-versions}

IPS Web服務由一組WSDL （Web服務描述語言）檔案支援，可從任何安裝IPS Web服務元件的IPS安裝存取。 每個IPS API版本都包含一個引用了版本化目標XML名稱空間的新WSDL檔案。 也支援舊版WSDL名稱空間，以便與現有應用程式回溯相容。

## WSDL存取 {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

存取Scene7 WSDL，如下所示。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

的預設值 `<IPS_webapp>` 是 `scene7`.

**服務位置**

服務URL是在IPS Web服務WSDL檔案的服務區段中指定的。 服務URL通常採用以下形式：

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**Dynamic Media地區的存取URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理位置 </p> </th> 
   <th colname="col2" class="entry"> <p>生產URL </p> </th> 
   <th colname="col3" class="entry"> <p>預備URL （用於生產前的開發和測試） </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>北美 </p> </td> 
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>歐洲、中東、亞洲 </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本/亞太地區 </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支援的WSDL {#section-ebbba69880f94e9c823f1147974eb404}

請記住，如果您想要使用最新版IPS API的功能，您可能需要修改程式碼。 IPS API支援下列版本的WSDL：

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API發行版本 </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API名稱空間 </p> </th> 
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
   <td colname="col1"> <p>4.0以前版本 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

現有應用程式若需修改以使用新功能，必須升級至最新的API版本，且可能需要變更現有程式碼。 如需詳細資訊，請參閱變更記錄。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**繫結**

IPS API Web服務僅支援SOAP繫結。

**支援的傳輸**

IPS API SOAP繫結僅支援HTTP傳輸。 使用HTTPSPOST方法提出所有SOAP請求。

**SOAP動作標頭**

若要處理要求，請將SOAPAction HTTP標頭設定為要求之作業的名稱。 WSDL繫結段落中的作業名稱屬性指定了名稱。

**訊息格式**

檔案/常值樣式用於所有輸入和輸出訊息，其型別以XML結構描述定義語言( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/))，並在WSDL檔案中指定。 所有型別都需要使用WSDL檔案中指定的目標名稱空間值的限定名稱。

**要求驗證**

在API要求中傳遞驗證認證的偏好方法是使用 `authHeader` 元素，如IPS API WSDL中所定義。

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
   <td colname="col2"> <p> 有效的IPS使用者電子郵件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 密码 </span> </p> </td> 
   <td colname="col2"> <p>使用者帳戶的密碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> 要求的選用地區設定。 另請參閱 <b>地區設定</b> 以取得詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> 正在呼叫應用程式名稱。 此引數為選用引數，但建議您將其納入所有請求中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> 正在呼叫應用程式版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> 啟用或停用回應XML的gzip壓縮的可選旗標。 依預設，如果HTTP Accept-Encoding標頭指出支援gzip，回應會進行gzip壓縮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> 用於覆寫錯誤回應的HTTP狀態碼的可選引數。 依預設，錯誤回應會傳回HTTP狀態碼500 （內部伺服器錯誤）。 有些使用者端平台(包括AdobeFlash)無法讀取回應內文，除非傳回狀態碼200 (OK)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

此 `authHeader` 元素一律會在名稱空間中定義 `http://www.scene7.com/IpsApi/xsd`，不論API版本為何。

以下範例為使用 `authHeader` 請求SOAP標頭中的元素：

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

**其他要求驗證方法**

如果由於某種原因，您的使用者端應用程式無法傳遞 `authHeader` SOAP標頭、API要求也可使用HTTP基本驗證指定認證（如RFC 2617所指定）。

對於HTTP基本驗證，每個SOAPPOST請求的HTTP標頭區段都必須包含表單的標頭：

`Authorization: Basic base64(<IPS_user_email>:<password>)`

位置 `base64()` 套用標準Base64編碼， `<IPS_user_email>` 是有效IPS使用者的電子郵件地址，並且 `<password>` 是使用者的密碼。

使用初始請求預先傳送Authorization標頭。 如果請求中未包含驗證認證， `IpsApiService` 未以的狀態代碼回應 `401 (Unauthorized)`. 相反地，狀態代碼為 `500 (Internal Server Error)` 傳回SOAP錯誤內文，指出無法驗證要求。

在IPS 3.8之前，已透過SOAP標頭使用實作驗證 `AuthUser` 和 `AuthPassword` 名稱空間中的元素 `http://www.scene7.com/IpsApi`. 例如：

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

此樣式仍支援回溯相容性，但已遭取代以支援 `authHeader` 元素。

**要求授權**

在呼叫者的認證通過驗證之後，檢查請求以確保呼叫者有權執行請求的操作。 授權是以呼叫者的使用者角色為基礎，可能也需要檢查目標公司、目標使用者和其他操作引數。 此外，Image Portal使用者必須屬於具有執行特定檔案夾和資產作業所需許可權的群組。 「作業」參考區段詳細說明每個作業的授權需求。

**SOAP請求和回應範例**

下列範例顯示完整的 `addCompany` 作業，包括HTTP標頭：

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

以及對應的回應：

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

**SOAP錯誤**

當作業遇到例外狀況時，會傳回SOAP錯誤作為SOAP訊息的主體來取代一般回應。 例如，如果非管理員使用者嘗試傳送先前的 `addCompany` 要求，則會傳回下列回應：

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
