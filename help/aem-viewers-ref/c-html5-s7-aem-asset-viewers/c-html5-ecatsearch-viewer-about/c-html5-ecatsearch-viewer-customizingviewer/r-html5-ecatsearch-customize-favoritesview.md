---
description: Vyn Favoriter består av en kolumn med miniatyrbilder.
seo-description: Vyn Favoriter består av en kolumn med miniatyrbilder.
seo-title: Vyn Favoriter
solution: Experience Manager
title: Vyn Favoriter
topic: Dynamic media
uuid: e9d0380e-3b08-45e4-8419-447df2e8de37
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Vyn Favoriter{#favorites-view}

Vyn Favoriter består av en kolumn med miniatyrbilder.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

Utseendet på favoritvybehållaren styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7favoritesview
```

Positionen och höjden på vyn Favoriter hanteras av vyn. i CSS är det bara möjligt att definiera bredden.

**CSS-egenskaper för vyn Favoriter**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg i vyn Favoriter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Vyns bredd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en Favoritvy som är 100 pixlar bred med en halvgenomskinlig grå bakgrund.

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

Avståndet mellan Favoriter-miniatyrbilder styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
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

Exempel - för att ställa in 10 pixelavstånd.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

Utseendet på enskilda miniatyrbilder styrs med följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**CSS-egenskaper för miniatyrbilderna Favoriter**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjden på miniatyrbilden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Miniatyrens kantlinje. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniatyrbilden har stöd för attributväljaren, som kan användas för att tillämpa olika skal på olika miniatyrlägen. `state` Motsvarar i synnerhet den miniatyrbild som användaren nyligen har valt `state="selected"` . `state="default"` motsvarar resten av miniatyrbilderna. Och `state="over"` används vid hovring med musen.

Exempel - Om du vill ställa in miniatyrbilder som är 75 x 75 pixlar har du en ljusgrå standardkant och en mörkgrå markerad kant.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Utseendet på miniatyrbildetiketten styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**CSS-egenskaper för etiketten Favoriter**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Teckensnittsnamn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Teckenstorlek. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in etiketter med ett Helvetica-teckensnitt med 14 pixlar.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

