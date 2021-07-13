---
description: Visningsprogrammet visar Favoriter-ikoner över huvudvyn på platser där det ursprungligen lades till av användaren.
solution: Experience Manager
title: Favoriter, effekt
feature: Dynamic Media Classic,Visningsprogram,SDK/API,eCatalog-sökning
role: Developer,User
exl-id: 7603c873-a2d1-4a24-85a6-8e56a1f207de
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Favoriter, effekt{#favorites-effect}

Visningsprogrammet visar Favoriter-ikoner över huvudvyn på platser där det ursprungligen lades till av användaren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utseendet på Favorit-ikonen styrs av följande CSS-klassväljare:

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon
```

**CSS-egenskaper för ikonen Favorit**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Bilden som visas för ikonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Ikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Ikonens höjd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ställ in en ikon med 36 x 36 pixlar för Favoriter.

```
.s7ecatalogsearchviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

På stationära datorer har komponenten stöd för attributväljaren `cursortype` som du kan använda för klassen `.s7favoriteseffect` och styr typen av markör baserat på den valda användaråtgärden. Följande `cursortype`-värden stöds:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>Den användare som visas lägger till en ny Favorit-ikon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>Den användare som visas tar bort en befintlig Favorit-ikon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view  </span> </p> </td> 
   <td colname="col2"> <p>Visas i normalläge när favoritredigering inte är aktiv. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ha olika musmarkörer för varje typ av komponentläge.

```
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogsearchviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```
