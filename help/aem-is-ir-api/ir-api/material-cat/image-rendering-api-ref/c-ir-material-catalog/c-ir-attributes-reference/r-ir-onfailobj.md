---
description: Felhantering av objektmarkeringsfel. Anger vilken åtgärd som ska vidtas om kommandot obj= misslyckas eftersom den angivna sökvägen inte kan matchas i vinjettobjektshierarkin.
seo-description: Felhantering av objektmarkeringsfel. Anger vilken åtgärd som ska vidtas om kommandot obj= misslyckas eftersom den angivna sökvägen inte kan matchas i vinjettobjektshierarkin.
seo-title: OnFailObj
solution: Experience Manager
title: OnFailObj
topic: Scene7 Image Serving - Image Rendering API
uuid: b9dcaf29-ffa5-47db-9c8c-d1809da73582
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 3%

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
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Behåll föregående markering. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Avmarkera; Alla försök att använda material eller visa/dölja objekt ignoreras. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
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
