---
description: Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla användargränssnittskontroller som är tillgängliga för videovisningsprogrammet, t.ex. uppspelnings-/pausknappen, volymkontroller osv.
solution: Experience Manager
title: Kontrollfält
feature: Dynamic Media Classic,visningsprogram,SDK/API,360 VR-video
role: Utvecklare,Affärsledare
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Kontrollfält{#control-bar}

Kontrollfältet är det rektangulära området som innehåller och sitter bakom alla användargränssnittskontroller som är tillgängliga för videovisningsprogrammet, t.ex. uppspelnings-/pausknappen, volymkontroller osv.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Kontrollfältet har alltid hela den tillgängliga visningsprogrambredden. Det går att ändra färgen, höjden och den lodräta positionen med CSS i förhållande till visningsprogrammets behållare.

Följande CSS-klassväljare styr kontrollfältets utseende:

```
.s7video360viewer .s7controlbar
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

**Exempel**  - Om du vill ställa in ett videovisningsprogram med ett grått kontrollfält som är 30 pixlar högt och som visas högst upp i visningsprogrammets behållare.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
