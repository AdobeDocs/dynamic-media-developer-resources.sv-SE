---
title: textAngle
description: Textåtergivningsriktning. Anger vinkeln som text som anges med textPs= placeras och återges i textrutan (definieras med size= eller textFlowPath=).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 102dbdc0-77b8-4c60-b456-6cf693e0b38b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# textAngle{#textangle}

Textåtergivningsriktning. Anger vinkeln som text som anges med textPs= placeras och återges i textrutan (definieras med size= eller textFlowPath=).

` textAngle= *`vinkel`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> vinkel </span> </p> </td> 
  <td class="stentry"> <p>Riktningsvinkel (grader). </p> </td> 
 </tr> 
</table>

Positiva värden roterar texten medsols och `textAngle=90` ritar texten uppifrån och ned.

## Egenskaper {#section-6d586a632daa4261a8ce62db56140b36}

Lagerattribut. Gäller för `layer=0` om `layer=comp`. Ignoreras om `textPs=` inte har angetts för det här lagret eller om `textPath=` har angetts.

## Standard {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` utan rotering.

## Se även {#section-dccc29ff33704061b2519b56b7be45fd}

[Textformatering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Textpositionering](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
