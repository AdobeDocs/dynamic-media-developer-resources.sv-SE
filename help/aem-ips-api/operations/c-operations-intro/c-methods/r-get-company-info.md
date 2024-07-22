---
description: Returnerar information om det angivna företaget inklusive företagshandtaget, företagsnamnet, rotsökvägen och förfallodatumet. Du måste ange antingen companyHandle eller companyName vars information du vill hämta.
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72bd223b-c99a-48a3-9c0a-d1af392d904c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# getCompanyInfo{#getcompanyinfo}

Returnerar information om det angivna företaget inklusive företagshandtaget, företagsnamnet, rotsökvägen och förfallodatumet. Du måste ange antingen companyHandle eller companyName vars information du vill hämta.

Syntax

## Auktoriserade användartyper {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-7dec8871c89a414c9f066adade1831d8}

**Indata (getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoriskt </p> </th> 
   <th colname="col4" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Antingen <span class="codeph"> <span class="varname"> companyHandle </span> </span> eller <span class="codeph"> <span class="varname"> companyName </span> </span> krävs. </p> </td> 
   <td colname="col4"> <p>Handtaget för det företag vars information du vill få. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Antingen <span class="codeph"> <span class="varname"> companyHandle </span> </span> eller <span class="codeph"> <span class="varname"> companyName </span> </span> krävs. </p> </td> 
   <td colname="col4"> <p>Namnet på det företag vars information du vill få. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Namn </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoriskt </p> </th> 
   <th colname="col4" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> typer:Company</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Hantera och annan information om företaget. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Detta kodexempel returnerar all information om ett företag genom att använda ett företagsnamn och en referens. Den returnerar data som liknar svaret som togs emot när ett företag skapades.

**Begäran**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**Svar**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```
