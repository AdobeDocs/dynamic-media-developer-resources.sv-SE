---
title: batchjobbinformationsstatus
description: Hämta sammanfattad status för ett skickat jobb.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b31bdbb-3c2c-4f7f-ba95-d3e710270be0
source-git-commit: 13991f71ab54d1003a79a496b861d53a61899bdc
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# batchjobbinformationsstatus{#batchjobbriefstatus}

Hämta sammanfattad status för ett skickat jobb.

Den här parametern:

<table id="simpletable_86E581DBB352479CB4CB531434D91E83"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jobid </span> </p> </td> 
  <td class="stentry"> <p>Jobb-ID som hämtades vid tidpunkten för överföringen. </p> </td> 
 </tr> 
</table>

Returnerar:

Kortfattad status för arbetet i XML-format. fel om jobbet är ogiltigt eller om jobbet har tagits bort.

## Exempel {#section-806460949bb043438ad4dd4e7ab74145}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobbriefstatus&jobid=1005907604914d8eb63126b98f7172n76a5]
