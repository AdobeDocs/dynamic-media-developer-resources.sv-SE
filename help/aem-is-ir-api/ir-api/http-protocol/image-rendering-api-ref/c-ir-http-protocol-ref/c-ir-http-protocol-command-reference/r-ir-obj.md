---
description: Markera objekt efter namn. Väljer den angivna vinjettgruppen efter namn och startar ett nytt MSS.
solution: Experience Manager
title: obj
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# obj{#obj}

Markera objekt efter namn. Väljer den angivna vinjettgruppen efter namn och startar ett nytt MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Gruppnamn eller sökväg/namn. </p> </td> 
 </tr> 
</table>

Undergrupper eller enskilda objekt kan markeras med en fullständig gruppsökväg (d.v.s. genom att ange namnet på målgruppen eller objektet som föregås av alla överordnade grupper, avgränsade med / (snedstreck).

Om ingen grupp/objekt med det angivna namnet hittas utförs åtgärden som anges i `attribute::OnObjFail`.

## Egenskaper {#section-9463b36e8ff74c81a70c7c2b58927430}

Markeringskommando; MSS-avgränsare. Objektmarkeringen är beständig tills ett annat objekt markeras, antingen med `obj=` eller `sel=`.

Grupp-/objektsökvägar och namn är inte skiftlägeskänsliga.

## Standard {#section-0c322850512c4896bb551856a549440e}

Den första gruppen i vinjetteringen som innehåller återgivningsbara objekt markeras automatiskt när en ny vinjettering öppnas.

## Se även {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [attribut::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
