---
description: Felhantering av markeringsfel. Anger vilken åtgärd som ska vidtas om sel=-kommandot misslyckas eftersom den angivna pixelplatsen inte ligger inom maskområdet för ett markeringsbart objekt.
seo-description: Felhantering av markeringsfel. Anger vilken åtgärd som ska vidtas om sel=-kommandot misslyckas eftersom den angivna pixelplatsen inte ligger inom maskområdet för ett markeringsbart objekt.
seo-title: OnFailSel
solution: Experience Manager
title: OnFailSel
topic: Scene7 Image Serving - Image Rendering API
uuid: 073b6651-970c-460c-b044-e3ef37cc677a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 3%

---


# OnFailSel{#onfailsel}

Felhantering av markeringsfel. Anger vilken åtgärd som ska vidtas om sel=-kommandot misslyckas eftersom den angivna pixelplatsen inte ligger inom maskområdet för ett markeringsbart objekt.

## Egenskaper {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Ärv från <span class="codeph"> standard::OnFailSel </span>. </p> </td> 
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

## Standard {#section-c25f458f9f8f4236963a95779529e664}

Ärvs från `default::OnFailSel` om inte definierat.

## Se även {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) ,  [attribut::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
