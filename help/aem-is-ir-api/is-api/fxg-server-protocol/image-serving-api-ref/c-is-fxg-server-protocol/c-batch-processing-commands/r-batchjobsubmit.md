---
description: Skicka ett nytt batchjobb.
solution: Experience Manager
title: batchjobbskicka
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ab2f6e4-cd68-4f1e-ab54-6f5e9bfc87cb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '38'
ht-degree: 0%

---

# batchjobbskicka{#batchjobsubmit}

Skicka ett nytt batchjobb.

Den här parametern:

<table id="simpletable_11A94D630A21426F9A1CEF5EB3B9E789"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobbdata </span> </p> </td> 
  <td class="stentry"> <p>XML-kodfragment med fullständiga jobbdata. </p> </td> 
 </tr> 
</table>

Returnerar:

<table id="simpletable_7C82E4A8520440F5A5ABBC1BCB286AB2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Jobbstatus </p> </td> 
  <td class="stentry"> <p>Om överföringen lyckades eller misslyckades. Jobb-ID i XML-format om det lyckades. </p> </td> 
 </tr> 
</table>

## Exempel {#section-3886e8352e26419c97b24df21ca7f6fd}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobsubmit&jobdata=<URLEncodedXMLFileContents>`
