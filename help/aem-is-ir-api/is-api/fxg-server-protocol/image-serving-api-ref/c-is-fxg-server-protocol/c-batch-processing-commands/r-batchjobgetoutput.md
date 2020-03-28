---
description: Hämta utdata från ett skickat jobb.
seo-description: Hämta utdata från ett skickat jobb.
seo-title: batchjobgetoutput
solution: Experience Manager
title: batchjobgetoutput
topic: Scene7 Image Serving - Image Rendering API
uuid: c2d49cc2-3223-4f0f-8ba7-4f74a5f76789
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobgetoutput{#batchjobgetoutput}

Hämta utdata från ett skickat jobb.

Den här parametern:

<table id="simpletable_D8AA325968AD4FAEA7B214F0CBBF3F08"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>Jobb-ID som hämtades vid tidpunkten för överföringen. </p> </td> 
 </tr> 
</table>

Returnerar:

PDF-utdata från jobbet direktuppspelas som svar på detta, fel om `jobid` är ogiltigt eller om jobbet har tagits bort.

## Exempel {#section-0319e615fa254132a9dab59351b4c252}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobgetoutput&jobid=1005907604914d8eb63126b98f7172n76a5]
