---
title: res
description: Upplösningsbaserad bildskalning. Skalar bilden till den önskade upplösningen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# res{#res}

Upplösningsbaserad bildskalning. Skalar bilden till den önskade upplösningen.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Målupplösning, vanligtvis i pixlar per tum (reell). </p> </td> 
 </tr> 
</table>

Skalningsfaktorn beräknas genom division *`val`* av `catalog::Resolution`. Observera att det här kommandot inte påverkar utskriftsupplösningen för svarsbilden.

Om du vill använda den här funktionen måste upplösningen för de ursprungliga källbilderna vara känd och anges i `catalog::Resolution`. Beroende på programmet kan upplösningsenheterna variera. För repeterbara 2D-texturer eller materialfärgrutor, t.ex. tapeter eller strukturer, kan upplösningen uttryckas som pixlar/tum eller pixlar/mm. Flygfoton och flygkartor kan betjänas bättre av pixlar/mils eller pixlar/km. De enheter som används för `catalog::Resolution` måste vara samma som de enheter som används för `res=`.

Förutom att hämta bilder med exakta upplösningar `res=` kan också användas för att kombinera flera bilder med samma upplösning, så att de objekt som visas i dessa bilder har rätt proportioner i förhållande till varandra.

>[!NOTE]
>
>Normalt ändras storleken på en sammansatt bild till målvisningsstorleken (anges av `wid=`, `hei=`, eller `attribute::DefaultPix`) innan den returneras till klienten. För att förhindra den här storleksändringen och få en bild med exakt den upplösning som anges av `res=`kan det vara nödvändigt att inaktivera vyskalning genom att explicit specificera `scl=1`. Detta instruerar servern att beskära den sammansatta bilden till målvisningsstorleken i stället för att skala den.

## Egenskaper {#section-fdbd16e59cff4952a3717146bc91412e}

Källbild/maskattribut. Ignoreras av lager som inte är kopplade till en källbild eller källmask. Tillämpas på lager 0 anges för `layer=comp`. Ignoreras om något `scale=` eller `size=` anges för samma lager.

## Standard {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Om inget anges, `scale=` eller `size=` bestämmer skalningsfaktorn, eller om inget av dem anges, används bilden utan skalning.

## Exempel {#section-eb06f333e08e4247971fb1b18922597b}

Hämta en texturbild med upplösningen 12 pixlar/tum som kan användas med bildåtergivning eller bildredigering. Vi anger förlustfritt PNG-format och bättre kvalitetsomsampling för bästa möjliga kvalitet,

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Se även {#section-1f8a8f11772e493ca803c4511f397a11}

[katalog::Upplösning](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
