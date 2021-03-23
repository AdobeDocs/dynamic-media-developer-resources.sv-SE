---
description: Hämta detaljerad status för ett skickat jobb.
seo-description: Hämta detaljerad status för ett skickat jobb.
seo-title: batchjobbdetaljstatusstatus
solution: Experience Manager
title: batchjobbdetaljstatusstatus
uuid: a79302ce-745b-44d8-9cb6-ed8d37530197
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# batchjobbdetaljerad status{#batchjobdetailedstatus}

Hämta detaljerad status för ett skickat jobb.

Den här parametern:

<table id="simpletable_9C379451927C4058834640377C0BD7A0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid  </span> </p> </td> 
  <td class="stentry"> <p>Jobb-ID som hämtades vid tidpunkten för överföringen. </p> </td> 
 </tr> 
</table>

Returnerar:

Detaljerad status för jobbet i XML-format; fel om `jobid` är ogiltigt eller om jobbet har tagits bort.

## Exempel {#section-55f463750afe4814b5fdbaa2f1aafab4}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdetailedstatus&jobid=1005907604914d8eb63126b98f7172n76a5`
