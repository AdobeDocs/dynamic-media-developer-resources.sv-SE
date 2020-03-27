---
description: Utdatafärgprofil.
seo-description: Utdatafärgprofil.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

Utdatafärgprofil.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profil</span></span> </p></td> 
  <td class="stentry"> <p>ICC-färgprofil. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span></span> </p></td> 
  <td class="stentry"> <p>perceptuell| relativ| mättnad| absolut </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> svartpunktComp</span></span> </p></td> 
  <td class="stentry"> <p>1 för att aktivera 0 för att inaktivera svartpunktskompensation. </p></td> 
 </tr> 
</table>

*`profile`* Anger den utdatafärgrymdsprofil som den återgivna bilden ska konverteras till om den inte är samma som arbetsprofilen. *`profile`* måste vara antingen en giltig `icc::Name` definierad i ICC-profilmappningen för en bildkatalog eller standardkatalog, eller en relativ sökväg till en profilfil (vanligtvis med [!DNL .icc]eller [!DNL .icm] suffix).

>[!NOTE]
>
>*`profile`* får inte innehålla &quot;,&quot;-tecken, även om det är HTTP-kodat.

*`renderIntent`* tillåter att standardåtergivningsmetoden åsidosätts.

*`blackpointComp`* aktiverar svartpunktskompensation om utdataprofilen har stöd för den här funktionen.

>[!NOTE]
>
>Alla färgkonverteringar har inte stöd för alla *`renderIntent`* och *`blackpointComp`* alternativ. Normalt gäller de här inställningarna bara när ICC-utdataprofilen karakteriserar en utdataenhet som en skrivare eller bildskärm. Vissa ICC-utdataprofiler stöder inte alla *`renderIntent`* alternativ.

## Egenskaper {#section-b4042623a8ea40248c11b2153e5906b1}

Kan inträffa var som helst i begäran. Ett fel returneras om bildtypen är angiven med `fmt=` inte matchar *`profile`*.

*`renderIntent`* och ignoreras *`blackpointComp`* om de inte är kompatibla med den angivna ICC-profilen.

Det är mer sannolikt att profiler för CMYK-utdataenheter har stöd för olika återgivningsmetoder.

## Standard {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Om färghantering är aktiverat och `icc=` inte är specificerat, kommer servern att leverera bilden konverterad till den utdataprofil ( `attribute::IccProfile*`) som matchar den bildtyp som har angetts med `fmt=`.

Om inget anges ärvs *`renderIntent`* från `attribute::IccRenderIntent`och *`blackpointComp`* ärvs från `attribute::IccBlackPointCompensation`.

## Se även {#section-37ef83149fd74345956a98f633cc0294}

[Färghantering](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribut::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribut::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribut::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
