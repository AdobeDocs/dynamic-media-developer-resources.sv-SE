---
title: Sekundärt kontrollfält
description: Det sekundära kontrollfältet är det rektangulära området som innehåller knapparna Första sidan och Sista sidan och en sidindikator när det är tillgängligt i CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e5d6abe8-0ae9-4ccd-b311-5895e09310b2
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---

# Sekundärt kontrollfält{#secondary-control-bar}

Det sekundära kontrollfältet är det rektangulära området som innehåller knapparna Första sidan och Sista sidan och en sidindikator när det är tillgängligt i CSS.

Som standard visas den endast på mobiltelefoner längst ned i visningsprogrammet. Den har alltid hela den tillgängliga visningsprogrambredden. Det går att ändra färgen, höjden och den lodräta positionen med CSS i förhållande till visningsbehållaren.

Utseendet på det sekundära kontrollfältet styrs med följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> övre </span> </p> </td> 
   <td colname="col2"> <p>Placera högst upp i visningsprogrammet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant </span> </p> </td> 
   <td colname="col2"> <p>Placera längst ned i visningsprogrammet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Huvudkontrollfältets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärgen för det sekundära kontrollfältet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in ett grått sekundärt kontrollfält som är 72 pixlar högt och placerat längst ned i visningsbehållaren.

```
.s7ecatalogsearchviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```
