---
title: flaggor
description: Använd flaggor. Anger ytterligare renderingsalternativ.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0c3f65e-2dec-4c35-8df4-8d111e81f3f0
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# flaggor {#flags}

Använd flaggor. Anger ytterligare renderingsalternativ.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Flaggvärde. </p></td> 
 </tr> 
</table>

Används för närvarande endast för kabinettmaterial.

`flags=0` (standard) Återger övre skåp med fasta dörrar.

`flags=1` Ritar upp övre skåp med glasdörrar (om vinjetteringen har skapats med glasdörrar).

## Egenskaper {#section-a2b00d7bb15e449ea85178acb92d8285}

Materialattribut. Ignoreras om det inte är ett kabinettmaterial eller om målkabinettobjektet inte tillåter glasdörrar.

## Standard {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` För inga glasdörrar.
