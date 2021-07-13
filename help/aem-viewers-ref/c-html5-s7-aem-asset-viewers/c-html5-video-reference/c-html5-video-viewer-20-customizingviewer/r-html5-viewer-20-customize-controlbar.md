---
description: Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla UI-kontroller som är tillgängliga för videovisningsprogrammet, t.ex. uppspelnings-/pausknappen, volymkontroller osv.
solution: Experience Manager
title: Kontrollfält
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Video
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Kontrollfält{#control-bar}

Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla UI-kontroller som är tillgängliga för videovisningsprogrammet, t.ex. uppspelnings-/pausknappen, volymkontroller osv.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Kontrollfältet har alltid hela den tillgängliga visningsprogrambredden. Det går att ändra färgen, höjden och den lodräta positionen med CSS i förhållande till visningsprogrammets behållare.

Följande CSS-klassväljare styr kontrollfältets utseende:

```
.s7videoviewer .s7controlbar
```

## CSS-egenskaper för kontrollfältet {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Placera från den övre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p> Placera från den nedre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Kontrollfältets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Kontrollfältets bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Om du vill ställa in ett videovisningsprogram med ett grått kontrollfält som är 30 pixlar högt och som visas högst upp i visningsprogrammets behållare.

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
