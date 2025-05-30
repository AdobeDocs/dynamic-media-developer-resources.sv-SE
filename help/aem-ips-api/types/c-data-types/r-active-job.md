---
title: ActiveJob
description: Ett jobb som körs på en server. Det är också en instans av ett schemalagt jobb.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3d878207-99e4-4c75-ab12-b38a37c82fb7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 0%

---

# [!DNL ActiveJob]{#activejob}

Ett jobb som körs på en server. Det är också en instans av ett schemalagt jobb.

Det finns jobb i tre lägen:

* Schemalagd att köras.
* Körs.
* Slutförd körning (och har redan skrivit information till en jobblogg).

Om du vill returnera jobbtypen anger du ett jobbtypsvärde. Du kan returnera följande jobb:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublish`
* `JobUploadDirectoryJob`
* `uploadUrlsJob`

## Parametrar {#section-6590fe864a434000822b9ec384784512}

<table id="table_1C4DDAB4EB1341FDA92B6F14E0132F75"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handla till företaget. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Hantera jobbet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Unikt namn för jobbet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> originalName </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Ursprungligt namn för typen <span class="codeph"> ActiveJob </span> som skickades med jobbet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Val av jobbtyper som returneras av systemet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> state </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Val av aktiva jobbtillstånd som returneras av systemet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> E-postadress till den användare som schemalagt jobbet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Språkinställningen för jobbloggsinformation och e-postlokalisering. <p>Ange språkinställningar som <span class="codeph"> &lt;språkkod&gt;[-&lt;landskod&gt;]</span>, där språkkoden är en kod med två bokstäver i gemener enligt ISO-639, och den valfria landskoden är en kod med två bokstäver i versaler enligt ISO-3166. Den nationella strängen för engelska (USA) skulle till exempel vara: <span class="codeph"> en-US</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Jobbbeskrivningen angavs ursprungligen i <span class="codeph"> submitJob</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverName </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Namnet på servern som kör jobbet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> startDate </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum, tid och tidszon för det aktiva jobbet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> totalSize </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Total storlek för det aktiva jobbet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progress </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Jobbförlopp (d.v.s. hur nära jobbet är att slutföra). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Ett textmeddelande som beskriver jobbförloppet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Datum, tid och tidszon för den senaste förloppsuppdateringen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskProgressArray </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:TaskProgressArray</span> </td> 
   <td colname="col3"> Asynkron information om aktivitetens förlopp. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Jobbinformation för en bild som visar publiceringsjobb. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingRenderJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageServingRenderJob</span> </td> 
   <td colname="col3"> Jobbinformation för en bild som återger publiceringsjobb. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:VideoPublishJob</span> </td> 
   <td colname="col3"> Jobbinformation för ett videopubliceringsjobb. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Jobbinformation för ett serverkatalogpubliceringsjobb. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UploadUrlsJob</span> </td> 
   <td colname="col3"> Jobbinformation för ett jobb för att ladda upp URL:er. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:RipPdfsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:OptimizeImagesJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ReprocessAssetsJob</span> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadPostJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:UploadPostJob</span> </td> 
   <td colname="col3"> Jobbdetaljer, spåra överföring till skrivbordet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:ExportJob</span> </td> 
   <td colname="col3">Tillåt auktoriserad export av tidigare överförda filer. Se <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-exportjob.html?lang=sv-SE" format="http" scope="external"> Exportera jobb </a>. </td> 
  </tr> 
 </tbody> 
</table>
