---
description: Det sekundära kontrollfältet är det rektangulära området som innehåller knapparna Första sidan och Sista sidan och en sidindikator när det är tillgängligt i CSS.
seo-description: Det sekundära kontrollfältet är det rektangulära området som innehåller knapparna Första sidan och Sista sidan och en sidindikator när det är tillgängligt i CSS.
seo-title: Sekundärt kontrollfält
solution: Experience Manager
title: Sekundärt kontrollfält
topic: Dynamic media
uuid: 9a91da6b-0d9b-4b4c-9659-86a64e624947
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# Sekundärt kontrollfält{#secondary-control-bar}

Det sekundära kontrollfältet är det rektangulära området som innehåller knapparna Första sidan och Sista sidan och en sidindikator när det är tillgängligt i CSS.

Som standard visas den endast på mobiltelefoner och finns längst ned i visningsprogrammet. Den har alltid hela den tillgängliga visningsprogrambredden. Det går att ändra färgen, höjden och den lodräta positionen med CSS i förhållande till visningsbehållaren.

Utseendet på det sekundära kontrollfältet styrs med följande CSS-klassväljare:

`.s7ecatalogviewer .s7secondarycontrols .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Placera högst upp i visningsprogrammet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p>Placera längst ned i visningsprogrammet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Huvudkontrollfältets höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Bakgrundsfärgen för det sekundära kontrollfältet. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - om du vill ställa in ett grått sekundärt kontrollfält som är 72 pixlar högt och som är placerat längst ned i visningsbehållaren.

```
.s7ecatalogviewer .s7secondarycontrols .s7controlbar {  
 bottom: 0px; 
 height: 72px; 
}
```

