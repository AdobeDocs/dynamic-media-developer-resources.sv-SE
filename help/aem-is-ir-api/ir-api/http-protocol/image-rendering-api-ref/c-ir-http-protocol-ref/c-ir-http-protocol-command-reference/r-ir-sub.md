---
title: sub
description: Delmarkering. Tillåter att olika material används på olika områden i det markerade objektet eller den markerade gruppen och att tidigare använt material tas bort.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 4%

---

# sub{#sub}

Delmarkering. Tillåter att olika material används på olika områden i det markerade objektet eller den markerade gruppen och att tidigare använt material tas bort.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Markera hela väggen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Markera den övre halvan av väggen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Markera den nedre halvan av väggen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Markera den övre kantlinjens område. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Markera gränsområdet för den mittersta väggen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Markera den nedre kantlinjens område. </p> </td> 
 </tr> 
</table>

Stöds för närvarande endast för väggobjekt. Avslutar ett föregående MSS och startar ett nytt MSS för det material som ska användas i det angivna delurvalet.

Ett material som anges för antingen den övre eller nedre väggen gäller hela väggen, såvida inte även ett annat material för den andra halvan av väggen har angetts.

## Egenskaper {#section-b202139d6d0847cc8d520a154104ab9d}

Markeringskommando; MSS-avgränsare.

## Standard {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Se även {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
