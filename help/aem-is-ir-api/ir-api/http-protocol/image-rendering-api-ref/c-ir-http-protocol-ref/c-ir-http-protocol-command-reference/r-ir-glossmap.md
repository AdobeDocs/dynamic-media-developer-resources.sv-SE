---
title: ordlista
description: Glanskarta. Tillhandahåller pixel-för-pixel-kontroll av glansigheten i en upprepningsbar textur, bakgrundsbild/kant eller dekal.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# ordlista {#glossmap}

Glanskarta. Tillhandahåller pixel-för-pixel-kontroll av glansigheten i en upprepningsbar textur, bakgrundsbild/kant eller dekal.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&klammerparentes;'is&lbrace;'<span class="varname"> isReq</span>'&rbrace;'&rbrace;|&lbrace;'&lbrace;'<span class="varname"> foreignReq</span>'&rbrace;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile </span> </span> </p></td> 
  <td class="stentry"> <p>Bildfil för glanskarta (gråskala). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq </span> </span> </p></td> 
  <td class="stentry"> <p>Begäran till Image Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Begär till en extern server. </p></td> 
 </tr> 
</table>

Gäller för material som metalliska målningseffekter, urklippta tapeter och kanter samt metalliska trådstrukturer.

Glanskartbilden måste vara 8-bitars gråskala och ha samma storlek som den primära bilden som anges med `src=`. Mer information finns i beskrivningen av [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca).

## Egenskaper {#section-26375672d69849be9b026cc93c3bc558}

Materialattribut. Stöds av repeterbara texturer, bakgrundsbilder och kanter samt dekorationer. Ignoreras av heltäckande färg, skåp och fönsteröverdrag. Mer information finns i [`gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca).

## Standard {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Ingen.

## Se även {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
