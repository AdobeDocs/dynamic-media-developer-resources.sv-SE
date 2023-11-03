---
title: obj
description: Markera objekt efter namn. Väljer den angivna vinjettgruppen efter namn och startar ett nytt MSS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# obj{#obj}

Markera objekt efter namn. Väljer den angivna vinjettgruppen efter namn och startar ett nytt MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Gruppnamn eller sökväg/namn. </p> </td> 
 </tr> 
</table>

Undergrupper eller enskilda objekt kan markeras med en fullständig gruppsökväg (det vill säga genom att ange namnet på målgruppen eller objektet som föregås av alla överordnade grupper, avgränsade med / (snedstreck).

Om ingen grupp/objekt med det angivna namnet hittas, anges åtgärden i `attribute::OnObjFail` tas.

## Egenskaper {#section-9463b36e8ff74c81a70c7c2b58927430}

Markeringskommando; MSS-avgränsare. Objektmarkeringen bevaras tills ett annat objekt markeras, antingen med `obj=` eller `sel=`.

Grupp-/objektsökvägar och namn är inte skiftlägeskänsliga.

## Standard {#section-0c322850512c4896bb551856a549440e}

Den första gruppen i vinjetteringen som innehåller återgivningsbara objekt markeras automatiskt när en ny vinjettering öppnas.

## Se även {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
