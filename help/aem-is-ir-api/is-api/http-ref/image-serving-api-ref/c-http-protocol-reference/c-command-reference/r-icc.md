---
description: Utdatafärgprofil.
seo-description: Utdatafärgprofil.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# icc{#icc}

Utdatafärgprofil.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentsvartpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>ICC-färgprofil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptuell|relativ|mättnad|absolut</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> svartpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 för att aktivera 0 för att inaktivera svartpunktskompensation. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> gitter</span></span> </p></td> 
  <td class="stentry"> <p>1 om du vill aktivera, 0 om du vill inaktivera gitter. </p></td> 
 </tr> 
</table>

*`object`* Anger den utdatafärgrymdsprofil som bilden ska konverteras till om den inte är samma som arbetsprofilen. *`profile`* måste vara antingen en giltig  `icc::Name` definierad i ICC-profilmappningen för en bildkatalog eller standardkatalog, eller en relativ sökväg till en profilfil (vanligtvis med  [!DNL .icc] eller  [!DNL .icm] suffix). Mer information finns i [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

>[!NOTE]
>
>*`object`* får inte innehålla &quot;,&quot;-tecken, även om det är HTTP-kodat.

*`renderIntent`* tillåter att standardåtergivningsmetoden åsidosätts.

*`blackpointComp`* aktiverar svartpunktskompensation om utdataprofilen har stöd för den här funktionen.

>[!NOTE]
>
>Alla färgkonverteringar har inte stöd för alla alternativ för *`renderIntent`* och *`blackpointComp`*. Normalt gäller de här inställningarna bara när ICC-utdataprofilen karakteriserar en utdataenhet som en skrivare eller bildskärm. Vissa ICC-utdataprofiler stöder inte alla *`renderIntent`*-alternativ.

Anteckning

*`dither`* aktiverar gitter (faktiskt felspridning), vilket kan leda till att färgreducering undviks eller minskas.

## Egenskaper {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Begär attribut. Servern returnerar ett fel om en bildtyp har angetts med `fmt=` som inte matchar *`profile`*.

*`renderIntent`* och  *`blackpointComp`* ignoreras om de inte är kompatibla med den angivna ICC-profilen. Det är mer sannolikt att profiler för CMYK-utdataenheter har stöd för olika återgivningsmetoder.

## Standard {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Om färghantering är aktiverat och `icc=` inte har angetts levererar servern bilden konverterad till utdataprofilen ( `attribute::IccProfile*`) som matchar bildtypen som har angetts med `fmt=`.

Om det inte anges ärvs *`renderIntent`* från `attribute::IccRenderIntent`, *`blackpointComp`* ärvs från `attribute::IccBlackPointCompensation` och *`dither`* ärvs från `attribute::IccDither`.

## Se även {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)  [object¥Color Management¥,¥ICC Profile Map ReferenceUnder,¥iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
