---
description: Skicka ett nytt batchjobb.
seo-description: Skicka ett nytt batchjobb.
seo-title: batchjobbskicka
solution: Experience Manager
title: batchjobbskicka
uuid: eb695666-fcaf-40bc-8b56-452819f058d2
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 0%

---


# batchjobsubmit{#batchjobsubmit}

Skicka ett nytt batchjobb.

Den här parametern:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobbdata  </span> </p> </td> 
  <td class="stentry"> <p>XML-kodfragment med fullständiga jobbdata. </p> </td> 
 </tr> 
</table>

Returnerar:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Jobbstatus </p> </td> 
  <td class="stentry"> <p>Huruvida överföringen lyckades eller misslyckades. om det lyckas, jobb-ID i XML-format. </p> </td> 
 </tr> 
</table>

## Exempel {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
