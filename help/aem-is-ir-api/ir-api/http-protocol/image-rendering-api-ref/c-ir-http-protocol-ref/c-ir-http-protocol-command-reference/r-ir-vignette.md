---
title: vinjettering
description: Vinjettfil. Anger vilken vinjett som ska användas för begäran.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# vinjettering{#vignette}

Vinjettfil. Anger vilken vinjett som ska användas för begäran.

`vignette=[ *`catId`*/] *`recId`*|[catId/] *`fil`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>ID för materialkatalog (matchas med <span class="codeph"> attribute::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Vinjett-ID (matchat med <span class="codeph"> vinjettering::ID</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fil</span> </p></td> 
  <td class="stentry"> <p>Filsökväg och namn för relativ vinjettering. </p></td> 
 </tr> 
</table>

Kan antingen ange en post för en vinjetteringskarta eller en vinjettfil. Fjärr-URL:er tillåts inte.

`vignette=` Kan användas som ett alternativ till att ange vinjett i URL-sökvägen för begäran. Används för att ange vinjetter med hjälp av variabler i mallar.

If *`catId`* anges inte, sessionskatalogen används.

## Egenskaper {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Kan inträffa var som helst i begäran. Åsidosätter den vinjett som har angetts med URL-sökvägen för begäran.

## Standard {#section-db0618d48bc84dc8abcc989550349ccc}

Ingen.

## Se även {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Materialkataloger](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [Anpassade variabler](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
