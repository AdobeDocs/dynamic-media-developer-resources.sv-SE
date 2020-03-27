---
description: Vinjettfil. Anger vilken vinjett som ska användas för denna begäran.
seo-description: Vinjettfil. Anger vilken vinjett som ska användas för denna begäran.
seo-title: vinjettering
solution: Experience Manager
title: vinjettering
topic: Scene7 Image Serving - Image Rendering API
uuid: 8bba4ad4-bd55-4c55-8ebf-585371cf33f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# vinjettering{#vignette}

Vinjettfil. Anger vilken vinjett som ska användas för denna begäran.

`vignette=[ *``*/] *``*|[catId/] *`catIdrecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>Materialkatalog-ID (matchas mot <span class="codeph"> attribut::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Vinjett-ID (matchas mot <span class="codeph"> vinjett::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fil</span> </p></td> 
  <td class="stentry"> <p>Filsökväg och namn för relativ vinjettering. </p></td> 
 </tr> 
</table>

Kan antingen ange en post för en vinjetteringskarta eller en vinjettfil. Fjärr-URL:er tillåts inte.

`vignette=` kan användas som ett alternativ till att ange vinjett i URL-sökvägen för begäran. Används främst för att ange vinjetter via variabler i mallar.

Om *`catId`* inte anges används sessionskatalogen.

## Egenskaper {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Kan inträffa var som helst i begäran. Åsidosätter den vinjett som har angetts med URL-sökvägen för begäran.

## Standard {#section-db0618d48bc84dc8abcc989550349ccc}

Ingen.

## Se även {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Materialkataloger](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [anpassade variabler](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
