---
description: 根据是否指定用户句柄，将特定用户或默认用户的口令设置为特定值。
seo-description: 根据是否指定用户句柄，将特定用户或默认用户的口令设置为特定值。
seo-title: setPassword
solution: Experience Manager
title: setPassword
topic: Dynamic Media Image Production System API
uuid: 78067f8d-4191-4580-a5a8-adb6edfcfab8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 7%

---


# setPassword{#setpassword}

根据是否指定用户句柄，将特定用户或默认用户的口令设置为特定值。

密码过期日期是可选的。 如果省略，则密码永不过期。

## 授权用户类型{#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*仅* 授权 `IpsAdmin` 用户类型对其他用户运行setPassword调用。

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## 参数 {#section-0531294341f7483d89dacaa393dd659a}

**输入(setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用户句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 口令  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>密码. </p> <p>对所选密码强制执行以下要求： </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">密码区分大小写。 </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">密码长度最小为8个字符。 </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">密码必须包含以下字符类中的一个或多个字符： 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">小写英语字符。 例如，<span class="codeph"> a b c d e </span>等 </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">大写英语字符。 例如，<span class="codeph"> A B C D E </span>等。 </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">数量. 例如，<span class="codeph"> 1 2 3 4 5 </span>等。 </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">特殊符号字符。 例如，您可以使用以下任意选项：<span class="codeph">“ ~ !@ # $ % ^ *()_ + - = { } | [ ] &amp; \ :" ;' &lt; &gt;, . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime  </span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>确定密码过期日期。 <p>注意： 为时区提供此字段的请求。 时区将调整为中央时间。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(setPasswordReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-23a6fbabdb3c4c3180076057e47ae567}

此代码示例创建用户密码。 密码永不过期，因为`passwordExpires`被省略。

**请求**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**响应**

无。
