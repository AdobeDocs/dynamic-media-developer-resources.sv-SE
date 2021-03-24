---
description: Glanskarta. Tillhandahåller pixel-för-pixel-kontroll av glansigheten i en upprepningsbar textur, bakgrundsbild/kant eller dekal.
solution: Experience Manager
title: ordlista
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---


# ordlista{#glossmap}

Glanskarta. Tillhandahåller pixel-för-pixel-kontroll av glansigheten i en upprepningsbar textur, bakgrundsbild/kant eller dekal.

`glossmap={ *``*| *`glossMapFileembeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;klammerparentes;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'  </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Bildfil för glanskarta (gråskala). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Begäran till Image Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq  </span> </span> </p></td> 
  <td class="stentry"> <p>Begär till en extern server. </p></td> 
 </tr> 
</table>

Gäller för material som metalliska färgeffekter, urklippta tapeter och kanter, metalliska trådstrukturer osv.

Glanskartbilden måste vara 8-bitars gråskala och ha exakt samma storlek som den primära bilden som anges med `src=`. Mer information finns i beskrivningen av [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca).

## Egenskaper {#section-26375672d69849be9b026cc93c3bc558}

Materialattribut. Stöds av repeterbara texturer, bakgrundsbilder och kanter samt dekorationer. Ignoreras av heltäckande färg, skåp och fönsteröverdrag. Mer information finns i [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca).

## Standard {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Ingen.

## Se även {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
