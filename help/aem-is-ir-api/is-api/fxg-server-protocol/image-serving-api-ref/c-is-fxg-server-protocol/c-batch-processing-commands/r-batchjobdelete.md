---
description: Ta bort utdata för ett jobb.
seo-description: Ta bort utdata för ett jobb.
seo-title: batchjobbta bort
solution: Experience Manager
title: batchjobbta bort
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# batchjobbdelete{#batchjobdelete}

Ta bort utdata för ett jobb.

Om ett jobb körs för tillfället stoppas det omedelbart och all bearbetningsinformation tas bort. Om jobbet har slutförts tas utdatafilen bort.

Den här parametern:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>Jobb-ID som hämtades vid tidpunkten för överföringen. </p></td> 
 </tr> 
</table>

Returnerar:

Status för jobbet när borttagningsbegäran togs emot, fel om `jobid` är ogiltigt eller om jobbet redan hade tagits bort.

## Exempel {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
