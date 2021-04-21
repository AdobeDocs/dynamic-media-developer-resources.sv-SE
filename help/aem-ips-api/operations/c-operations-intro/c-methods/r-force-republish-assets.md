---
description: Återställer publiceringsstatusen för en eller flera resurser för att tvinga resursen att publiceras på nytt i nästa publiceringsjobb.
solution: Experience Manager
title: forceRepublishAssets
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# forceRepublishAssets{#forcerepublishassets}

Återställer publiceringsstatusen för en eller flera resurser för att tvinga resursen att publiceras på nytt i nästa publiceringsjobb.

Syntax

## Auktoriserade användartyper {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**Indata (forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Hantera företaget som innehåller resurser som ska återställas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> publicera omFiler</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Anger att filerna för resursen publiceras på nytt till leveransservrarna. Standardvärdet är <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolesk</span> </td> 
   <td colname="col3"> <p>Nej </p> </td> 
   <td colname="col4"> <p>Anger att katalogmetadata som används för att hantera resursen synkroniseras för att garantera att den är aktuell. Den här parametern används för att lösa konkurrensvillkor som kan uppstå vid nästan samtidiga uppdateringar av samma post. Standardvärdet är <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:HandleArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>En array med referenser till resurser vars publiceringsstatus ska återställas. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Array med publiceringstillståndsuppdateringar. </p> </td> 
  </tr> 
 </tbody> 
</table>

