---
title: Överföra resurser via HTTP POST till UploadFile-servern
description: Överför resurser till [!DNL Dynamic Media] Klassisk innebär en eller flera HTTP-POST-begäranden som ställer in ett jobb för att koordinera all loggaktivitet som är associerad med de överförda filerna.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Överföra resurser via HTTP POST till UploadFile-servern{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

När du överför resurser till Dynamic Media Classic måste du ange en eller flera HTTP-POSTER som ställer in ett jobb för att koordinera all loggaktivitet som är kopplad till de överförda filerna.

Använd följande URL för att komma åt UploadFile-servern:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Alla POSTER som begär ett överföringsjobb måste komma från samma IP-adress.

**Åtkomst till URL:er för Dynamic Media-regioner**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geografisk plats </p> </th> 
   <th colname="col2" class="entry"> <p>Produktions-URL </p> </th> 
   <th colname="col3" class="entry"> <p>Mellanlagrings-URL (används för utveckling och testning av förproduktion) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nordamerika </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Mellanöstern, Asien </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Asien/Stillahavsområdet </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Överföringsjobbets arbetsflöde {#section-873625b9512f477c992f5cdd77267094}

Överföringsjobbet består av en eller flera HTTP POST som använder en vanlig `jobHandle` för att korrelera bearbetning till samma jobb. Varje begäran `multipart/form-data` kodad och består av följande formulärdelar:

>[!NOTE]
>
>Alla POSTER som begär ett överföringsjobb måste komma från samma IP-adress.

|  Formulärdel för HTTP-POST  |  Beskrivning  |
|---|---|
| `auth`  |   Obligatoriskt. Ett XML authHeader-dokument som anger autentisering och klientinformation. Se **Begär autentisering** under [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Valfritt. Du kan inkludera en eller flera filer som ska överföras vid varje begäran om POST. Varje fildel kan innehålla en filnamnsparameter i Content-Disposition-huvudet som används som målfilnamn i IPS om ingen `uploadPostParams/fileName` -parametern har angetts. |

|  Formulärdel för HTTP-POST   |  uploadPostParams-elementnamn   |  Typ   |  Beskrivning   |
|---|---|---|---|
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna)   |   `companyHandle`  |  `xsd:string`  | Obligatoriskt. Hantera till det företag som filen överförs till.  |
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna) | `jobName`  |  `xsd:string`  | Antingen `jobName` eller `jobHandle` krävs. Namn på överföringsjobbet.  |
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna) | `jobHandle`  |  `xsd:string`  | Antingen `jobName` eller `jobHandle` krävs. Hantera ett överföringsjobb som har startats i en tidigare begäran.  |
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna) | `locale`  |  `xsd:string`  | Valfritt. Språk- och landskod för lokalisering.  |
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna) | `description`  |  `xsd:string`  | Valfritt. Beskrivning av jobbet.  |
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna) | `destFolder`  |  `xsd:string`  | Valfritt. Sökväg till målmappen om du vill lägga till prefix till en filename-egenskap, särskilt för webbläsare och andra klienter som inte har stöd för fullständiga sökvägar i ett filnamn.  |
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna) | `fileName`  |  `xsd:string`  | Valfritt. Målfilens namn. Åsidosätter filename-egenskapen. |
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna) | `endJob`  |  `xsd:boolean`  | Valfritt. Standardvärdet är false. |
| `uploadParams` (Obligatoriskt. En XML `uploadParams` dokument som anger överföringsparametrarna) | `uploadParams`  |  `types:UploadPostJob`  | Valfritt om detta är en efterföljande begäran för ett befintligt aktivt jobb. Om det finns ett befintligt jobb, `uploadParams` ignoreras och de befintliga jobböverföringsparametrarna används. Se [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

I `<uploadPostParams>` blocket är `<uploadParams>` -block som anger bearbetningen av de inkluderade filerna.

Se [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Även om du kan anta att `uploadParams` -parametern kan ändras för enskilda filer som en del av samma jobb, vilket inte är fallet. Använd samma `uploadParams` parametrar för hela jobbet.

Den initiala POSTEN för ett nytt överföringsjobb ska ange `jobName` -parameter, helst med ett unikt jobbnamn för att förenkla efterföljande jobbstatuskontrollfrågor och jobbloggfrågor. Ytterligare POST-begäranden för samma överföringsjobb ska ange `jobHandle` parameter i stället för `jobName`, med `jobHandle` värdet som returnerades från den ursprungliga begäran.

Den slutliga POSTEN för ett överföringsjobb ska ange `endJob` parametern är true så att inga framtida filer POSTed för det här jobbet inte finns. Detta innebär i sin tur att jobbet kan slutföras omedelbart efter att alla POSTed-filer har importerats. Annars går jobbet ut om inga fler begäranden om POST tas emot inom 30 minuter.

## UploadPOST-svar {#section-421df5cc04d44e23a464059aad86d64e}

Svarstexten är en XML-POST för en lyckad begäran `uploadPostReturn` -dokument, enligt XSD:n i följande:

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

The `jobHandle` returneras skickas i `uploadPostParams`/ `jobHandle` -parameter för efterföljande POSTER för samma jobb. Du kan också använda den för att avfråga jobbstatus med `getActiveJobs` eller för att fråga efter jobbloggarna med `getJobLogDetails` operation.

Om det uppstår ett fel när POSTEN bearbetas består svarstexten av en av API-feltyperna enligt beskrivningen i [Fel](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Exempelbegäran om POST {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## Exempel på svar från POSTEN - lyckad {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## Exempel på svar från POSTEN - fel {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
