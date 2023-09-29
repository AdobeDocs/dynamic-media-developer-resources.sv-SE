---
title: batchjobbta bort
description: Ta bort utdata för ett jobb.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9aca6693-32ac-4abd-9595-95bce60050ec
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# batchjobbta bort{#batchjobdelete}

Ta bort utdata för ett jobb.

Om ett jobb körs för tillfället stoppas det omedelbart och all bearbetningsinformation tas bort. Om jobbet har slutförts tas utdatafilen bort.

Den här parametern:

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> job_id</span> </p> </td> 
  <td class="stentry"> <p>Jobb-ID som hämtades vid tidpunkten för överföringen. </p></td> 
 </tr> 
</table>

Returnerar:

Status för jobbet när borttagningsbegäran togs emot, felmeddelande om `jobid` är ogiltigt eller så har jobbet redan tagits bort.

## Exempel {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

`http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5`
