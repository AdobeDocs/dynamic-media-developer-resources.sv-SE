---
description: Opacitet. Anger materialets opacitet.
seo-description: Opacitet. Anger materialets opacitet.
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# opac{#opac}

Opacitet. Anger materialets opacitet.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Materialopacitet (procent). 0...100 </p> </td> 
 </tr> 
</table>

Följande material-/objektkombinationer har stöd för variabel opacitet:

* Enfärgade och repeterbara texturer som används på texturerbara överlappningsobjekt.
* Fönsteromslagsmaterial som används på fönsteromfattande ramobjekt.
* Decaler som används på texturerbara objekt eller väggobjekt.

Om materialet innehåller en bild med en alfakanal kan `opac=` användas för att göra bilden mer genomskinlig, men inte mer ogenomskinlig.

## Egenskaper {#section-352f7b82ede54159b6afb90ae4b559ec}

Materialattribut. Ignoreras om den aktuella objektmarkeringen eller materialet inte stöder opacitet.

## Standard {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, för ett helt ogenomskinligt material (om bilden inte innehåller någon alfakanal).
