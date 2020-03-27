---
description: Användning av bildmask. Anger hur masken eller alfakanalen i bilden används för åtgärder i bilden (till exempel color=). När det anges i ett effektlager kan effekten användas på bakgrundsområdet i det överordnade lagret eller på hela rektangeln för det överordnade lagret.
seo-description: Användning av bildmask. Anger hur masken eller alfakanalen i bilden används för åtgärder i bilden (till exempel color=). När det anges i ett effektlager kan effekten användas på bakgrundsområdet i det överordnade lagret eller på hela rektangeln för det överordnade lagret.
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Scene7 Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# maskUse{#maskuse}

Användning av bildmask. Anger hur masken eller alfakanalen i bilden används för åtgärder i bilden (till exempel color=). När det anges i ett effektlager kan effekten användas på bakgrundsområdet i det överordnade lagret eller på hela rektangeln för det överordnade lagret.

`maskUse=norm|invert|off`

I följande tabell visas effekten av `maskUse=` beroende på tillgänglighet och typ av mask (alfakanal) som är associerad med lagerbilden.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Värde</b> </th> 
   <th class="entry"> <b> Ingen mask</b> </th> 
   <th class="entry"> <b> Oassocierad alfa (eller separat maskbild)</b> </th> 
   <th class="entry"> <b> Associerad (förmultiplicerad) alfa</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> av </span> </p> </td> 
   <td> <p> Ogenomskinlig bildram </p> </td> 
   <td> <p> Ogenomskinlig bildram </p> </td> 
   <td> <p> Förgrundsområde för en bild över en rektangel fylld med helsvart </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norm </span> </p> </td> 
   <td> <p> Ogenomskinlig bildram </p> </td> 
   <td> <p> Bildens förgrundsområde </p> </td> 
   <td> <p> Förgrundsområde för bild eller lager </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> invertera </span> </p> </td> 
   <td> <p> Dolt lager </p> </td> 
   <td> <p> Bildens bakgrundsområde </p> </td> 
   <td> <p> Bakgrundsområde i bild eller lager fyllt med solid svart </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f36ad1af348e45aeb3eb336544df30b0}

Bild- eller lagerattribut. Gäller för lager 0 om `layer=comp`. Om det anges i ett effektlager ändrar kommandot den mask som ärvs från det överordnade lagret.

Beteendet för `maskUse=` är odefinierat och stöds inte när det anges med text eller enfärgade lager när ingen bildmask kan användas (anges med `mask=` eller `catalog::Mask`).

## Standard {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Exempel {#section-daa371e9be5547368ff6772342acba0a}

Färga en bilds bakgrundsområde. bildens förgrund definieras av en separat maskbild. Detta uppnås genom att den färgade bildbakgrunden läggs i lager ovanpå om den oförändrade bilden:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Se även {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
