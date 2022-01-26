---
title: Kontrollfält
description: Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla användargränssnittskontroller som är tillgängliga för videovisningsprogrammet, till exempel knappen Spela upp/Paus, volymkontroller osv.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Kontrollfält{#control-bar}

Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla användargränssnittskontroller som är tillgängliga för videovisningsprogrammet, till exempel knappen Spela upp/Paus, volymkontroller osv.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Kontrollfältet har alltid hela den tillgängliga visningsprogrambredden. Det går att ändra färgen, höjden och den lodräta positionen med CSS i förhållande till visningsprogrammets behållare.

Följande CSS-klassväljare styr kontrollfältets utseende:

```
.s7mixedmediaviewer .s7controlbar
```

## CSS-egenskaper för kontrollfältet {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Kontrollfältets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Kontrollfältets bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Om du vill ställa in ett blandat visningsprogram med ett grått kontrollfält som är 30 pixlar högt.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
