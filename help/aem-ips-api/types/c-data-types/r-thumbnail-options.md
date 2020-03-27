---
description: En valfri typ där du kan välja en viss videobildruta som ska användas som miniatyrbild.
seo-description: En valfri typ där du kan välja en viss videobildruta som ska användas som miniatyrbild.
seo-title: Miniatyrbildsalternativ
solution: Experience Manager
title: Miniatyrbildsalternativ
topic: Scene7 Image Production System API
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Miniatyrbildsalternativ{#thumbnailoptions}

En valfri typ där du kan välja en viss videobildruta som ska användas som miniatyrbild.

Syntax

## Parametrar {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>Anger tiden (i millisekunder från videostarten) för bildrutan som du vill använda som videominiatyr. Värdena varierar från 0 till slutet av videon. <p>Obs! Systemet använder den första bildrutan i videon som miniatyrbild om du anger tidpunkten felaktigt. Se <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> Mediealternativ</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```

