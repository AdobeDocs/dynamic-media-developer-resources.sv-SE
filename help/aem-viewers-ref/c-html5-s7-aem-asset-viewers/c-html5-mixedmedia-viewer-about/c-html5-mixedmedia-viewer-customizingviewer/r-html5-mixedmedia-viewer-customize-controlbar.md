---
description: Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla användargränssnittskontroller som är tillgängliga för videovisningsprogrammet, t.ex. uppspelnings-/pausknappen, volymkontroller osv.
seo-description: Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla användargränssnittskontroller som är tillgängliga för videovisningsprogrammet, t.ex. uppspelnings-/pausknappen, volymkontroller osv.
seo-title: Kontrollfält
solution: Experience Manager
title: Kontrollfält
uuid: 7b7dccb3-6c64-4342-aac7-82c769561902
feature: Dynamic Media Classic,Visningsprogram,SDK/API,Mixa medieuppsättningar
role: Utvecklare,Affärsledare
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---


# Kontrollfält{#control-bar}

Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla användargränssnittskontroller som är tillgängliga för videovisningsprogrammet, t.ex. uppspelnings-/pausknappen, volymkontroller osv.

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

Om du vill ställa in ett blandat visningsprogram med ett grått kontrollfält som är 30 pixlar högt.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

