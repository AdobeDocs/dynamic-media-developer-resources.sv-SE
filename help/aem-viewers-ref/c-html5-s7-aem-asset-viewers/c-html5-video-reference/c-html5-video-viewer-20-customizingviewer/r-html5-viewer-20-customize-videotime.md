---
title: Videotid
description: Videotiden är den numeriska visning som visar aktuell tid och varaktighet för den video som spelas upp.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83491281-aff4-411a-a5a2-42e2454fd375
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Videotid{#video-time}

Videotiden är den numeriska visning som visar aktuell tid och varaktighet för den video som spelas upp.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Teckensnittsfamiljen för videotid, teckensnittsstorleken och teckensnittsfärgen är några av de egenskaper som CSS kan styra. Den kan också placeras, i förhållande till kontrollfältet som innehåller den, av CSS.

Utseendet på videotiden styrs av följande CSS-klassväljare:

```
.s7videoviewer .s7videotime
```

## CSS-egenskaper för videotid {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> övre </span> </p> </td> 
   <td colname="col2"> <p>Placera från den övre kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger </span> </p> </td> 
   <td colname="col2"> <p>Placera från den högra kanten, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Bredden på videotidskontrollen. Den här egenskapen krävs för Internet Explorer 8 eller senare för att fungera korrekt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Den teckensnittsfamilj som ska användas för visningstexten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Den teckensnittsstorlek som ska användas för visningstexten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> färg </span> </p> </td> 
   <td colname="col2"> <p>Teckenfärgen som ska användas för visningstexten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Ange att videotstiden ska vara ljusgrå (hexadecimal `#BBBBBB`), storleksanpassad till 12 pixlar, placerad 15 pixlar från kontrollfältets överkant och 80 pixlar från kontrollfältets högra kanter.

```
.s7videoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
