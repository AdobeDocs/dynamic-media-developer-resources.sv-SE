---
description: Skickar ett jobb till systemet.
seo-description: Skickar ett jobb till systemet.
seo-title: submitJob
solution: Experience Manager
title: submitJob
topic: Dynamic Media Image Production System API
uuid: d3a83b59-bcd7-4ae9-b1ee-e515fc3c9261
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---


# submitJob{#submitjob}

Skickar ett jobb till systemet.

Syntax

## Auktoriserade användartyper {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-31a07dbccf964850883e817384499459}

**Indata (submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
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
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Företagshandtag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Hantera till användaren som skickade jobbet. </p> <p> <p>Obs! Systemet skickar e-post till användaren som anges av <span class="codeph"> userHandle</span>. Om <span class="codeph"> userHandle</span> inte anges får personen som skickade jobbet e-postmeddelandena. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Jobbnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Språkinställningen som används för jobbloggsinformation och e-postlokalisering. </p> <p>Språk anges som <span class="codeph"> &lt;språkkod&gt;</span> och <span class="codeph"> [&lt;landskod&gt;]</span>, där språkkoden är en gemen, tvåbokstavskod enligt ISO-639, och den valfria landskoden är en versal, tvåbokstavskod enligt ISO-3166. Den nationella strängen för engelska (USA) skulle till exempel vara: en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Datum och tid då jobbet ska köras. </p> <p>Obs!  Ange tidszonen med begäran. Tidszoner justeras till tidzonen för mål-IPS-servern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Anger när jobbet ska köras. </p> <p> Kan vara en <span class="codeph"> cron</span>-sträng som kör jobbet med återkommande intervall. </p> <p>Schemat är alltid relativt serverns lokala tidszon. I IPS-dokumentationen finns information om det anpassade schemaformatet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Jobbbeskrivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ExportJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Exportera tidigare överförda filer. </p> <p>Se <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Information om en bild som visar publiceringsjobb. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Information om ett publiceringsjobb för bildåtergivning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:VideoPublishJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Information om ett videopubliceringsjobb. </p> <p>Se <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Information om ett serverkatalogpubliceringsjobb. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UploadDirectoryJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Information om ett uppladdningskatalogjobb. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UploadUrlsJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Information om ett överförings-URL-jobb. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:OptimizeImagesJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:RipPdfsJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatiseradSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> <p>Bearbeta en resurslista i uppsättningar med hjälp av automatiska uppsättningsskript. </p> <p>Se <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (submitJobReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`jobHandle`*` | `xsd:string` | Ja | Jobbreferens. |

## Exempel {#section-40ac77d14adf4588ba2575be6879b2d2}

Det här kodexemplet skickar en bild som visar publiceringsjobb till IPS och returnerar en jobbreferens. Välj bara en typ av jobb i förfrågan. Eftersom `userHandle` utelämnades skickas e-postmeddelanden till användaren som skickade jobbet. Det här exempeljobbet körs omedelbart eftersom `execTime` och `execSchedule` utelämnades.

**Begäran**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**Svar**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## Anteckningar {#section-0f3078e503a249aeb6f3d662a51f036a}

Du kan ange högst ett av `execTime` och `execSchedule`. Om inget av det godkänns körs jobbet omedelbart. Du kan bara använda något av följande:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`

