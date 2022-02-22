---
title: opac
description: Opacitet. Anger materialets opacitet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# opac{#opac}

Opacitet. Anger materialets opacitet.

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Materialopacitet (procent). 0...100 </p> </td> 
 </tr> 
</table>

Följande material-/objektkombinationer har stöd för variabel opacitet:

* Enfärgade och repeterbara texturer som används på texturöverlappande objekt.
* Fönsteromslagsmaterial som används på fönsteromfattande ramobjekt.
* Decaler som används på texturobjekt eller väggobjekt.

Om materialet innehåller en bild med en alfakanal, `opac=` kan användas för att göra bilden mer genomskinlig, men inte mer ogenomskinlig.

## Egenskaper {#section-352f7b82ede54159b6afb90ae4b559ec}

Materialattribut. Ignoreras om den aktuella objektmarkeringen eller materialet inte stöder opacitet.

## Standard {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`, för ett helt ogenomskinligt material (om bilden inte innehåller någon alfakanal).
