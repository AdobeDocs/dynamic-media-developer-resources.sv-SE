---
description: Felhantering av objektmarkeringsfel. Anger vilken åtgärd som ska vidtas om kommandot obj= misslyckas eftersom den angivna sökvägen inte kan matchas i vinjettobjektshierarkin.
solution: Experience Manager
title: OnFailObj
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# OnFailObj{#onfailobj}

Felhantering av objektmarkeringsfel. Anger vilken åtgärd som ska vidtas om kommandot obj= misslyckas eftersom den angivna sökvägen inte kan matchas i vinjettobjektshierarkin.

## Egenskaper {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Ärv från <span class="codeph"> standard::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Behåll föregående markering. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Avmarkera; Alla försök att använda material eller visa/dölja objekt ignoreras. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Returnera ett fel. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Markera standardgruppen (den första gruppen i vinjetteringshierarkin som innehåller återgivningsbara objekt). </p> </td> 
 </tr> 
</table>

## Standard {#section-a5a95a2b4a204a4eae350e5b544d1513}

Ärvs från `default::OnFailObj` om inte definierat.

## Se även {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [attribut::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
