---
description: IPS-webbtjänsten stöds av en uppsättning WSDL-dokument (Web Services Description Language) som nås från alla IPS-installationer där IPS-webbtjänstkomponenten är installerad. Varje IPS API-version innehåller en ny WSDL-fil som refererar till ett versionshanterat mål-XML-namnutrymme. Tidigare versioner av WSDL-namnutrymmen stöds också för bakåtkompatibilitet med befintliga program.
seo-description: IPS-webbtjänsten stöds av en uppsättning WSDL-dokument (Web Services Description Language) som nås från alla IPS-installationer där IPS-webbtjänstkomponenten är installerad. Varje IPS API-version innehåller en ny WSDL-fil som refererar till ett versionshanterat mål-XML-namnutrymme. Tidigare versioner av WSDL-namnutrymmen stöds också för bakåtkompatibilitet med befintliga program.
seo-title: WSDL-versioner för IPS-webbtjänst
solution: Experience Manager
title: WSDL-versioner för IPS-webbtjänst
topic: Scene7 Image Production System API
uuid: 3443bb91-1663-4686-b20a-94c372f0026e
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---


# WSDL-versioner för IPS-webbtjänst{#ips-web-service-wsdl-versions}

IPS-webbtjänsten stöds av en uppsättning WSDL-dokument (Web Services Description Language) som nås från alla IPS-installationer där IPS-webbtjänstkomponenten är installerad. Varje IPS API-version innehåller en ny WSDL-fil som refererar till ett versionshanterat mål-XML-namnutrymme. Tidigare versioner av WSDL-namnutrymmen stöds också för bakåtkompatibilitet med befintliga program.

## WSDL-åtkomst {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Gå till Scene7 WSDL:er enligt nedan.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

Standardvärdet för `<IPS_webapp>` är `scene7`.

**Tjänstplats**

Tjänstens URL anges i tjänstavsnittet i WSDL-dokumentet för IPS-webbtjänsten. Tjänstens URL har vanligtvis följande format:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**Åtkomst till URL:er för Scene7-regioner**

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Mellanöstern, Asien </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Asien/Stillahavsområdet </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## WSDL:er {#section-ebbba69880f94e9c823f1147974eb404} som stöds

Kom ihåg att du kanske måste ändra koden om du vill använda funktionerna i den senaste versionen av IPS API. IPS-API:t stöder WSDL:er för följande versioner:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API-versionsversion </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API-namnutrymme </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pre-4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Befintliga program som måste ändras för att kunna använda nya funktioner måste uppgradera till den senaste API-versionen och kan behöva göra ändringar i befintlig kod. Mer information finns i ändringsloggen.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Bindningar**

IPS API-webbtjänsten stöder endast SOAP-bindning.

**Transporter som stöds**

IPS API SOAP-bindningen stöder endast HTTP-transport. Gör alla SOAP-begäranden med HTTPS-POST-metoden.

**SOAP-åtgärdshuvud**

Om du vill bearbeta en begäran anger du HTTP-huvudet SOAPAction till namnet på den begärda åtgärden. Åtgärdsnamnattributet i WSDL-bindningsavsnittet anger namnet.

**Meddelandeformat**

Formatet document/literal används för alla in- och utdatameddelanden med typer som är baserade på definitionsspråket XML-schema ( [http://www.w3.org/TR/xmlschema-0/](http://www.w3.org/TR/xmlschema-0/)) och som anges i WSDL-filen. Alla typer kräver kvalificerade namn med det målnamnutrymmesvärde som anges i WSDL-filen.

**Begär autentisering**

Den metod som rekommenderas för att skicka autentiseringsuppgifter i API-begäranden är att använda elementet `authHeader` som definierats i IPS API WSDL.

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

**Fält**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> användare  </span> </p> </td> 
   <td colname="col2"> <p> Giltig e-postadress för IPS-användare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lösenord  </span> </p> </td> 
   <td colname="col2"> <p>Lösenord för användarkonto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale  </span> </p> </td> 
   <td colname="col2"> <p> Valfri språkinställning för begäran. Mer information finns i <b>Språk</b>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName  </span> </p> </td> 
   <td colname="col2"> <p> Anropar programnamn. Den här parametern är valfri, men vi rekommenderar att du tar med den i alla förfrågningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion  </span> </p> </td> 
   <td colname="col2"> <p> Anropar programversion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse  </span> </p> </td> 
   <td colname="col2"> <p> Valfri flagga för att aktivera eller inaktivera gzip-komprimering för XML-svar. Som standard är svaren gzip-komprimerade om rubriken HTTP Accept-Encoding anger stöd för gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> errorHttpStatusCode  </span> </p> </td> 
   <td colname="col2"> <p> Valfri parameter för att åsidosätta HTTP-statuskoden för felsvar. Som standard returnerar felsvar HTTP-statuskod 500 (Internt serverfel). Vissa klientplattformar, inklusive Adobe Flash, kan inte läsa svarstexten om inte statuskoden 200 (OK) returneras. </p> </td> 
  </tr> 
 </tbody> 
</table>

`authHeader`-elementet definieras alltid i namnutrymmet `http://www.scene7.com/IpsApi/xsd`, oavsett API-version.

Följande är ett exempel på hur du använder elementet `authHeader` i en SOAP-huvud för begäran:

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

**Andra autentiseringsmetoder för begäranden**

Om det av någon anledning inte är möjligt för klientprogrammet att skicka SOAP-huvudet `authHeader` kan API-begäranden även ange autentiseringsuppgifter med HTTP Basic-autentisering (enligt RFC 2617).

För grundläggande HTTP-autentisering måste HTTP-huvudavsnittet i varje SOAP-POST innehålla en rubrik i formuläret:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Där `base64()` använder standardkodningen Base64 är `<IPS_user_email>` e-postadressen för en giltig IPS-användare och `<password>` är användarens lösenord.

Skicka auktoriseringshuvudet företrädesvis med den initiala begäran. Om inga autentiseringsuppgifter ingår i begäran svarar inte `IpsApiService` med statuskoden `401 (Unauthorized)`. I stället returneras statuskoden `500 (Internal Server Error)` med en SOAP-felkod som anger att begäran inte kunde autentiseras.

Före IPS 3.8 implementerades autentisering via SOAP-huvudet med elementen `AuthUser` och `AuthPassword` i namnutrymmet `http://www.scene7.com/IpsApi`. Exempel:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Det här formatet stöds fortfarande för bakåtkompatibilitet, men har ersatts med elementet `authHeader`.

**Begär auktorisering**

När anroparens autentiseringsuppgifter har autentiserats kontrolleras begäran för att säkerställa att anroparen har behörighet att utföra den begärda åtgärden. Auktoriseringen baseras på användarrollen för anroparen och kan även kräva kontroll av målföretaget, målanvändaren och andra åtgärdsparametrar. Dessutom måste användare av Image Portal tillhöra en grupp med de behörigheter som krävs för att utföra vissa mapp- och resursåtgärder. I referensavsnittet Drift finns information om behörighetskraven för varje åtgärd.

**Exempel på SOAP-begäran och -svar**

I följande exempel visas en fullständig `addCompany`-åtgärd, inklusive HTTP-rubriker:

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

Och motsvarande svar:

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

**SOAP-fel**

När en åtgärd påträffar ett undantagsvillkor, returneras ett SOAP-fel som texten i SOAP-meddelandet i stället för det normala svaret. Om en icke-admin-användare till exempel försöker skicka föregående `addCompany`-begäran returneras följande svar:

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

