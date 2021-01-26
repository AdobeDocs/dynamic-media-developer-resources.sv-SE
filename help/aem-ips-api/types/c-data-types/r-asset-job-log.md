---
description: Information om en jobbloggpost som är associerad med en viss resurs. Data returneras av getAssetJobLogs.
seo-description: Information om en jobbloggpost som är associerad med en viss resurs. Data returneras av getAssetJobLogs.
seo-title: AssetJobLog
solution: Experience Manager
title: AssetJobLog
topic: Dynamic Media Image Production System API
uuid: 0dd65da1-f358-4d9a-98a2-abfb036347e3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# AssetJobLog{#assetjoblog}

Information om en jobbloggpost som är associerad med en viss resurs. Data returneras av getAssetJobLogs.

Syntax

## Parametrar {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Jobbreferens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Jobbnamn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3">Meddelande i jobbloggen. <p><span class="codeph"> Fältet </span> logMessagersvar är lokaliserat baserat på  <span class="codeph"> </span> authHeaderlocale-fältet. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Typ av jobb i loggposten. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> submitUserEmail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> e-postadress till den användare som skickade jobbet. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> logDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Jobbdatum. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> auxArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> typer:JobLogDetailArray</span> </td> 
   <td colname="col3"> Matris med hjälpjobbloggmeddelanden för varje jobblogg. </td> 
  </tr> 
 </tbody> 
</table>

