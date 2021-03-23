---
description: Använd flaggor. Anger ytterligare renderingsalternativ.
seo-description: Använd flaggor. Anger ytterligare renderingsalternativ.
seo-title: flaggor
solution: Experience Manager
title: flaggor
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# flaggor{#flags}

Använd flaggor. Anger ytterligare renderingsalternativ.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Flaggvärde. </p></td> 
 </tr> 
</table>

Används för närvarande endast för kabinettmaterial.

`flags=0` (standard) återger övre skåp med fasta dörrar.

`flags=1` återger övre skåp med glasdörrar (om vinjetteringen har skapats med glasdörrar).

## Egenskaper {#section-a2b00d7bb15e449ea85178acb92d8285}

Materialattribut. Ignoreras om det inte är ett kabinettmaterial eller om målkabinettobjektet inte tillåter glasdörrar.

## Standard {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` utan glasdörrar.
