---
description: Lägger till ett företag i systemet.
solution: Experience Manager
title: addCompany
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# addCompany{#addcompany}

Lägger till ett företag i systemet.

Skickar namnet på det företag som ska läggas till i systemet och skickar om företaget ska förfalla eller inte.

När den här åtgärden anropas får systemet en `*`companyInfo`*`-typ som innehåller en företagsreferens och beskrivande fält. Om det begärda företagsnamnet redan finns i systemet genereras ett `ipsApiFault`.

## Auktoriserade användartyper {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-c64a21b72585447880760db9e7a12ccb}

**Indata (addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Namnet på företaget som ska läggas till. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> förfaller</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Företagets förfallodatum. Ange tidszonen med begäran för det här fältet. Tidszoner justeras till Central Time. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:sträng</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Hantera namn, rotsökväg, utgångsdatum och tid för det nya företaget. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-4c8f1bb40d154c77a7b410468206e52b}

I det här exemplet visas en begäran om att lägga till ett företag i IPS-systemet och svaret med detaljerad information om det tillagda företaget som behövs för att utföra andra åtgärder.

**Begäran**

```java
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**Svar**

```java
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```

