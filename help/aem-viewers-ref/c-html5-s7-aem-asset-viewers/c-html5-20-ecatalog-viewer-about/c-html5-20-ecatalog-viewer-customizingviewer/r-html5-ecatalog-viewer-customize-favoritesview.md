---
title: Vyn Favoriter
description: Vyn Favoriter består av en kolumn med miniatyrbilder.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Vyn Favoriter{#favorites-view}

Vyn Favoriter består av en kolumn med miniatyrbilder.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

Utseendet på behållaren för vyn Favoriter styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7favoritesview
```

Positionen och höjden på vyn Favoriter hanteras av vyn. I CSS går det bara att definiera bredden.

**CSS-egenskaper för vyn Favoriter**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg i favoritvyn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Vyns bredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Så här ställer du in en favoritvy som är 100 pixlar bred med en halvgenomskinlig grå bakgrund:

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

Avståndet mellan Favoriter-miniatyrbilder styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**CSS-egenskaper för miniatyrbilderna Favoriter**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal </span> </p> </td> 
   <td colname="col2"> <p> Storleken på den lodräta marginalen runt varje miniatyrbild. Det faktiska mellanrummet för miniatyrbilder är lika med summan av den övre och nedre marginalen som är inställd för <span class="codeph"> .s7miniatyrcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Så här ställer du in tio pixelavstånd:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

Utseendet på enskilda miniatyrbilder styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**CSS-egenskaper för miniatyrbilderna Favoriter**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrbildens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på miniatyrbilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> kant </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrens kantlinje. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniatyrbilden stöder attributväljaren `state` som kan användas för att tillämpa olika skal på olika miniatyrlägen. I synnerhet motsvarar `state="selected"` den miniatyrbild som nyligen valts av användaren. Attributet `state="default"` motsvarar resten av miniatyrbilderna. Och attributet `state="over"` används vid hovring med musen.

Exempel - Om du vill ställa in miniatyrbilder som är 75 x 75 pixlar har du en ljusgrå standardkantlinje och en mörkgrå markerad kantlinje:

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Utseendet på miniatyrbildetiketten styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**CSS-egenskaper för etiketten Favoriter**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Typsnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - Så här ställer du in etiketter med ett Helvetica®-teckensnitt på 14 pixlar:

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
